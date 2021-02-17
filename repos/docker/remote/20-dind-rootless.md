## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:26d2592b50c5d940b5017cb5c3ec16e59e3f6ad577a622fedf5d80f6984842f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ca7f3a372161c52294bdbd477db0911573eb1b170f6bce9aa3ea741f47f26e87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102248970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331ed15d0d4ac7f8b124984bc4993e8fc9aad91b6a98a9a9dbd94b59ed237609`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:43:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 17 Feb 2021 21:43:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 Feb 2021 21:43:05 GMT
ENV DOCKER_VERSION=20.10.3
# Wed, 17 Feb 2021 21:43:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.3.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 17 Feb 2021 21:43:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 17 Feb 2021 21:43:12 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:43:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Feb 2021 21:43:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 17 Feb 2021 21:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:43:14 GMT
CMD ["sh"]
# Wed, 17 Feb 2021 21:43:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 17 Feb 2021 21:43:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 17 Feb 2021 21:43:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Wed, 17 Feb 2021 21:43:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 17 Feb 2021 21:43:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:43:23 GMT
VOLUME [/var/lib/docker]
# Wed, 17 Feb 2021 21:43:24 GMT
EXPOSE 2375 2376
# Wed, 17 Feb 2021 21:43:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 Feb 2021 21:43:24 GMT
CMD []
# Wed, 17 Feb 2021 21:43:30 GMT
RUN apk add --no-cache iproute2
# Wed, 17 Feb 2021 21:43:31 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 17 Feb 2021 21:43:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 17 Feb 2021 21:43:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.3.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 17 Feb 2021 21:43:35 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 17 Feb 2021 21:43:36 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 17 Feb 2021 21:43:36 GMT
USER rootless
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94caa5d1da7043140e78e14956c22154f75708f44c1c1367ac20cc5a8be71e8b`  
		Last Modified: Wed, 17 Feb 2021 21:44:58 GMT  
		Size: 2.1 MB (2051413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10a29983da5ea49c724d6c132f4d3dc6c130fe7148e4dd9fc258c34fa210f0a`  
		Last Modified: Wed, 17 Feb 2021 21:44:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b071e807615fb6b532dfdd17f2a8e762342b7c7fab8bbe4a4a5955b6d96cf446`  
		Last Modified: Wed, 17 Feb 2021 21:45:11 GMT  
		Size: 69.5 MB (69464299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e312d1fdaab9b3c93108fea6ae5669f6d02901ecb9058c69c26593aee6f5552c`  
		Last Modified: Wed, 17 Feb 2021 21:44:57 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22fb1b38bf3caf7fae8aad8e222981e7966663ecee232b6334e76249468e122`  
		Last Modified: Wed, 17 Feb 2021 21:44:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c60ac175054247b429aa833807d437b110d11a1bdde9d6ec24a8d164625291`  
		Last Modified: Wed, 17 Feb 2021 21:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91afbfdd7b778c4bcfb1fc9f2d924472ec7b3b5e54791e67aa381c4886d16641`  
		Last Modified: Wed, 17 Feb 2021 21:45:20 GMT  
		Size: 6.6 MB (6610375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babfe5fbbe656c5603a4e594447041fb6b8765352a706152ff18a50e3a13bf99`  
		Last Modified: Wed, 17 Feb 2021 21:45:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c24736699a6eae917e05f208d8a6450d5c98b08a66fc175c6579de3a9fbf68`  
		Last Modified: Wed, 17 Feb 2021 21:45:18 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c37595645aaccbdfdc23d0f2ecd36c298273ee86bc09dbbf3c622172496630`  
		Last Modified: Wed, 17 Feb 2021 21:45:18 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c21e8b762513c5ace7fcfbf9b6bbb199919f71985bcf3fb35b54e6c55c4f90e`  
		Last Modified: Wed, 17 Feb 2021 21:45:26 GMT  
		Size: 1.1 MB (1131695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466cc2385925ccfb2ea10ee184657188719db9518c01d0b30c18afcf368d7ea2`  
		Last Modified: Wed, 17 Feb 2021 21:45:25 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec963c634b0c7fb262998a39209def79829061660dd395807504c3d677e56175`  
		Last Modified: Wed, 17 Feb 2021 21:45:25 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f51783dde770256dbe32d76f1f8b41e8e67a43203c60e8dad23be3020bedd6`  
		Last Modified: Wed, 17 Feb 2021 21:45:34 GMT  
		Size: 20.2 MB (20171367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197274cbf35c0a629d9f3fa6e5929b80399ab10367c74a8d7d968d8fb1afd799`  
		Last Modified: Wed, 17 Feb 2021 21:45:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
