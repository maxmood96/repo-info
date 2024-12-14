## `docker:cli`

```console
$ docker pull docker@sha256:561338cb111f09a755c9c28e00b66a2466a3dacd88bca6f2f0aeaf909e95730a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:167c735d631b00384e268f1dd1230ada3bdcac915e749be562481fc37d7cf5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68472707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37409751f89a9183b99563f929bf21325fa6cfcf287679826ec502c1202c3ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:30ad0a07ac64a65ddcd433aeab8a1e559fa50327cb85fa12c22c6b26bdf8763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d0aa13057ebc4ae8e2594681075d7484b2d6e2aa8f0972640a33edf65f20fa`

```dockerfile
```

-	Layers:
	-	`sha256:87259a40baf16e0ae65ac41ce9f8eec992f0fec996d1f945f3c11306b74847e1`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:850519e09ac90396d48c2260b38db241f84f74acb4d372f03ae988d8b1419014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63604936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7f1cecb9a3b1e66edb8ea720a313bd0d7ad69900fee316c2b572c0b2464e12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2d2e4a9727681cfe5637fed05f28442cfeb4e3d4c74b54d1666deea18dbb2f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbfe47a312b92570b77592a48ed008e485b15bb45396495a529a8a455775092`

```dockerfile
```

-	Layers:
	-	`sha256:a14543e98fa59723762ef528b045c1706dfa299cb0a2db5d3c0c940e7ab6e645`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4b6e4baf1ab15df1260382122b976234e24237558bc65513671571609a18bc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62625308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0518d1dd421d96cd8f33089a34770da57b68c2740d3b9523f761895f742ed317`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:7cdeed720491a6c79999649859d8812011a8a80f99517f4940721f3b106ce4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7cd806863913b1082373e133d60b368631c92a06b92de0243c5876387a0a79`

```dockerfile
```

-	Layers:
	-	`sha256:843f0814593e40fbce871757fbea33ed8b9899f195a215342068a202ad2e0ed3`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a73907930d8ea382a8bfacc5362eb0640cb90f7416b75e42c24bb018694c19dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64440237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71be0f3c62209a33bbb2557f941d3e6e819568152fb39d16dba4e50fa13c6f14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4089d1cdec8b176b873a1d1e877c8bae7d65f093b06b8fbfe1d3e96d0a10cfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e62058998eb61300889bd4e4372fdfce6cc78bde26e2baaa436fcb4b10b0863`

```dockerfile
```

-	Layers:
	-	`sha256:93a1a3e41ef910ab186cf149424caadafef5cf4a7c34e68f789ab980b0483245`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json
