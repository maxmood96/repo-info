## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:2f47b4d6e394e4f9f5160eb36c286aebf11584bf1da816cf1b297c2f195b1b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:1c26d3c47a014d94cfaabd027a80746b07758426a660ead0633e0131996cc883
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101563895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b999295ebf616fc73703872721abef4cfbf1879dd0856a6f6d3b978467bc34d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:29:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 05:29:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:29:34 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 05:29:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 05:29:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 05:29:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:29:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 05:29:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 05:29:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:29:42 GMT
CMD ["sh"]
# Sat, 12 Dec 2020 18:12:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 12 Dec 2020 18:12:31 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 12 Dec 2020 18:12:31 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Sat, 12 Dec 2020 18:12:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 12 Dec 2020 18:12:32 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Sat, 12 Dec 2020 18:12:33 GMT
VOLUME [/var/lib/docker]
# Sat, 12 Dec 2020 18:12:33 GMT
EXPOSE 2375 2376
# Sat, 12 Dec 2020 18:12:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 12 Dec 2020 18:12:33 GMT
CMD []
# Sat, 12 Dec 2020 18:12:39 GMT
RUN apk add --no-cache iproute2
# Sat, 12 Dec 2020 18:12:40 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Sat, 12 Dec 2020 18:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Sat, 12 Dec 2020 18:12:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Sat, 12 Dec 2020 18:12:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Sat, 12 Dec 2020 18:12:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 12 Dec 2020 18:12:44 GMT
USER rootless
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db28d0fdbf69ee580b35224bf77ef5e71f9a061c0aafab87064af9708035d9d`  
		Last Modified: Fri, 11 Dec 2020 05:31:33 GMT  
		Size: 2.0 MB (2039048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292df0bc6bf3350f306af7623bc14f00386239bb27303d3047104b9cfdb55460`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e060f4bd70b333ccaa7ae441b42f1068621b39bbe8eb9c71b5a4e06d10b4ff3`  
		Last Modified: Fri, 11 Dec 2020 05:31:46 GMT  
		Size: 69.5 MB (69457871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e8d568a22304aafab5a456040525abd0b705efad0b6e60e64847ebe1c6e4e6`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6ef1a942a0f6b2ab0993eecb7ce30d31f06af50a2ae40893e1a160c9a0892`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2312dd95470aa8eaccef80bbca7892390ca777559b50fab574e65147a35107fc`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74c897205648b865ec45efcc0c0be8a3ccf9f3f3f60cc1383d5564c72302e20`  
		Last Modified: Sat, 12 Dec 2020 18:13:33 GMT  
		Size: 6.0 MB (5997645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa8e83a7aeb20771ef165f19449f2733ae1aee4c6efe28b6b2e4109ef65baa8`  
		Last Modified: Sat, 12 Dec 2020 18:13:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b1eb2027ff8834916826431c1bdd26901ee758dfb9877c38275a4e62239295`  
		Last Modified: Sat, 12 Dec 2020 18:13:32 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36cacd847e245cd8b2f813f5cba87f6b5fff177d7845e4cb1b290d27466ebe6`  
		Last Modified: Sat, 12 Dec 2020 18:13:32 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f5711cd4996f3deeaaad8bd8359abc05d090ed218ce3d4d126907d533fa135`  
		Last Modified: Sat, 12 Dec 2020 18:13:40 GMT  
		Size: 1.1 MB (1092847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232394c94602c3faf4ad2645879d44a4f9263f6c6c74ed11cc4f437a2cd2ea5c`  
		Last Modified: Sat, 12 Dec 2020 18:13:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0593b8f932913d0b7dd33ac6dfa40794a5d20e449753ef21ea509f73f41a8`  
		Last Modified: Sat, 12 Dec 2020 18:13:40 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d290602014138dee291b47ff62dc195f4ad4de18d47790cb85620acd75b0406`  
		Last Modified: Sat, 12 Dec 2020 18:13:44 GMT  
		Size: 20.2 MB (20171371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fbdf89349e40fb1d5471f7dc3c9d0973463d3baea4c2cfbe6877728aa60bae`  
		Last Modified: Sat, 12 Dec 2020 18:13:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
