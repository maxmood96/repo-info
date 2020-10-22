## `docker:dind-rootless`

```console
$ docker pull docker@sha256:59782050d360caa5bd75d0903706d728c8a67b779417b604e83fc10a029763c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7e88eb523dd692072fa8f8467730df9be4dfff616475dc7c64dacf5f7527088f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96546514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c6e32408b16047783a9c6d9f474e715f92aa295f6c0ed3c32c7e3c857ed71e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:15:44 GMT
ENV DOCKER_VERSION=19.03.13
# Thu, 22 Oct 2020 03:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.13.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.13.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.13.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 22 Oct 2020 03:15:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 22 Oct 2020 03:15:50 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 22 Oct 2020 03:15:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 22 Oct 2020 03:15:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 22 Oct 2020 03:15:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 03:15:51 GMT
CMD ["sh"]
# Thu, 22 Oct 2020 03:15:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 22 Oct 2020 03:15:58 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 22 Oct 2020 03:15:59 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 22 Oct 2020 03:16:00 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 22 Oct 2020 03:16:00 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 22 Oct 2020 03:16:00 GMT
VOLUME [/var/lib/docker]
# Thu, 22 Oct 2020 03:16:00 GMT
EXPOSE 2375 2376
# Thu, 22 Oct 2020 03:16:00 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 22 Oct 2020 03:16:01 GMT
CMD []
# Thu, 22 Oct 2020 03:16:06 GMT
RUN apk add --no-cache iproute2
# Thu, 22 Oct 2020 03:16:07 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 22 Oct 2020 03:16:08 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 22 Oct 2020 03:16:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-19.03.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Thu, 22 Oct 2020 03:16:10 GMT
ENV ROOTLESSKIT_VERSION=0.10.0
# Thu, 22 Oct 2020 03:16:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Thu, 22 Oct 2020 03:16:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 22 Oct 2020 03:16:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 22 Oct 2020 03:16:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dafad2182aae29aeec9c17a0eb7b8a418902147a74d41a5408bd331ad7b61a`  
		Last Modified: Thu, 22 Oct 2020 03:16:58 GMT  
		Size: 62.7 MB (62668352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa711733414defdf599caa6bbb097b529419ba31f862069350c2c4e32c3bf04`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058f73b55e4ba2b1e9c395241302653a08228f457e8c8adf0b51426de7c2cfef`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9c664faf126b51772616bb78c98f55f404b3c3d9271621229cc765faa17bfb`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0b6491c6e7d75eaa16d14ff8cc3de7012a35ff667afd4f77f65611c720a09a`  
		Last Modified: Thu, 22 Oct 2020 03:17:10 GMT  
		Size: 6.0 MB (5958697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee22c609ee43d4142523e04df614a5f5b5c25db5baa46a607ae0d18f23553715`  
		Last Modified: Thu, 22 Oct 2020 03:17:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22785feb8270b25a73018501153ef150e5001ce47a21e941e387daedd9e8c78c`  
		Last Modified: Thu, 22 Oct 2020 03:17:07 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b32acae31f672ec626bd97b0b90fa20e42305812895c2489de852ecef41dd`  
		Last Modified: Thu, 22 Oct 2020 03:17:07 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86be94fb716bd921a99d2da5e3f84f1196b372ef44e1c918fe885441eff68dae`  
		Last Modified: Thu, 22 Oct 2020 03:17:23 GMT  
		Size: 1.1 MB (1092666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fcd6dd81a070ee71c04c4099361f7bd7f38d28673e200f25492173ac80cc24`  
		Last Modified: Thu, 22 Oct 2020 03:17:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874903fdd7381dd30cc132733e97f34dcd327e407ee393f016f675c8d55ab4fa`  
		Last Modified: Thu, 22 Oct 2020 03:17:21 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ec0dacdd920477f9a31d173f4b0b37ab3c178c75f1dbd971388f9e3e72c071`  
		Last Modified: Thu, 22 Oct 2020 03:17:23 GMT  
		Size: 9.1 MB (9109459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd00f82a50f75858f60eb1c6e54277ebac8d72053e11d1f9ea8118a9628f185`  
		Last Modified: Thu, 22 Oct 2020 03:17:23 GMT  
		Size: 12.9 MB (12873254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7184d4deb1336ff71595f8cf39daf7ac7ae58080896ae0371f516edef09661a8`  
		Last Modified: Thu, 22 Oct 2020 03:17:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
