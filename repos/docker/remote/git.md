## `docker:git`

```console
$ docker pull docker@sha256:a9ec8dce9cdab5c0d82690840373f70a0fcc9a2b2f5ad5a0d38147b2d2d8ef93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:f268a917b445d72291c0fc9668f4b1b741f75841665ef7b61620eb97d66ace9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75087137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c7cb5cd3da7d62f8b618fa5ff42c6766ef3df03b7e0fd3f61495134bf8209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:02:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cc0be1abc487b32db89139b7ed719bedb57d01764e80fadf1efc3d736128e1`  
		Last Modified: Fri, 12 Nov 2021 22:03:57 GMT  
		Size: 6.6 MB (6630719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:abd4f25a749ebaac21635348b5e8db17d1d7cc5bcfa3b437e730b4178177cd2f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69115687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb4264b475ad1b401f8776fd4d94293173ddd396cf1a88a5fb4372947b3ef3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:12:04 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 13 Nov 2021 11:12:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 18 Nov 2021 09:17:16 GMT
ENV DOCKER_VERSION=20.10.11
# Thu, 18 Nov 2021 09:17:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.11.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.11.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.11.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.11.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 18 Nov 2021 09:17:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 18 Nov 2021 09:17:25 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 18 Nov 2021 09:17:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Nov 2021 09:17:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 18 Nov 2021 09:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Nov 2021 09:17:28 GMT
CMD ["sh"]
# Thu, 18 Nov 2021 09:18:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233f664f6e365c4259a38e7cfe3c14e234ab45f15847cc874a88b510f66a132f`  
		Last Modified: Sat, 13 Nov 2021 11:13:40 GMT  
		Size: 1.9 MB (1909969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501a1c7cbdd3e377ff292e68f9ced99315b84c85398591633343352948bbc291`  
		Last Modified: Sat, 13 Nov 2021 11:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b50fed93df89351d596ab08fab482a174aa37a86d61cdeef150162665a67a80`  
		Last Modified: Thu, 18 Nov 2021 09:18:59 GMT  
		Size: 57.7 MB (57746015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21638a3c07c5ebd6977bcc9c75e0ac36c2a82b761fc51a8aee313c9a9d7ed46`  
		Last Modified: Thu, 18 Nov 2021 09:18:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e37a1bae185ca8552a00efd7984a74bc595d0dac82ab81e945615f5a0b29af`  
		Last Modified: Thu, 18 Nov 2021 09:18:49 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c4e38c2d1b6603791a26f4dad582d554c306fb4c8c4218e0d537da3b8af6a`  
		Last Modified: Thu, 18 Nov 2021 09:18:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d06f8877e01ae57a21f32e8cdd5b66ffc3fdf70cfb5c8036a429db1ed15e12`  
		Last Modified: Thu, 18 Nov 2021 09:20:04 GMT  
		Size: 6.7 MB (6740174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
