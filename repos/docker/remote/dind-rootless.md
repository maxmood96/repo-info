## `docker:dind-rootless`

```console
$ docker pull docker@sha256:140d629d80a53ee558d442d6e6425fcae76c687b0a910262af867b0a9ad1fc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a433dd7b2f9cd8b8e5fc4655b675584cce9f712da996c6f46165d8495efbc69f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101524712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4b3576648314bb2a5af93388a92239da8e49f71c9a73477ac9ddb51b4b3c90`
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
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
# Thu, 10 Dec 2020 16:34:30 GMT
RUN apk add --no-cache iproute2
# Thu, 10 Dec 2020 16:34:31 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 10 Dec 2020 16:34:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 10 Dec 2020 16:34:35 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 10 Dec 2020 16:34:35 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 10 Dec 2020 16:34:35 GMT
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
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9134a376d14301f855d03ff3808689d77e7b85cea7ab8213478ab7ca7d8789c`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 1.1 MB (1092671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63fd1383e6fbafd721d12e0c99aea5120a31aa52aefb5aa1808a41ffadb9`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772148c137c8bd1474c6946b0192b3f7a786c997d26b80affcb79d17444eff62`  
		Last Modified: Thu, 10 Dec 2020 16:35:40 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c5ac8ed7ead1c35040d0bb2392053119d1646b27dae4a766925ebaa248f388`  
		Last Modified: Thu, 10 Dec 2020 16:35:45 GMT  
		Size: 20.2 MB (20171371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ddf2da86992920ab4482bf8a52843988196d895f07619d775f4f1258a50cc0`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
