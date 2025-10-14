## `docker:29-rc-cli`

```console
$ docker pull docker@sha256:dff391de58c6d11da023066ba8aa7ced8b8b6f2ef6634ed038e20950e0793b7f
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

### `docker:29-rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:0f916b92f4b78f8774370c97d41ce5f0e63b58fc52ae1ea9283621bd96b1eca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75542241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a4d1d97335ecfba51d0efebfbbb2d361a22cda207f56e9afaaebecf7fe2e72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_VERSION=29.0.0-rc.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 14 Oct 2025 15:11:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bbca4dac63dda61c15f026e41128ceed724306ef1926d3af5d649611f35255`  
		Last Modified: Tue, 14 Oct 2025 18:16:12 GMT  
		Size: 8.2 MB (8205949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5cd71a5c62247f7db914287661a8deb65e131718c0084f0d71f362ef99d296`  
		Last Modified: Tue, 14 Oct 2025 18:16:10 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3005f77ab24b95f065333d3986387a41de710df6d63d9bee7955e0e8b0d08a`  
		Last Modified: Tue, 14 Oct 2025 18:16:14 GMT  
		Size: 19.7 MB (19747043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aa0124a3341a72d24da8293b5701732bf7eab02a8e49d385a7fd7e13d9a519`  
		Last Modified: Tue, 14 Oct 2025 18:16:13 GMT  
		Size: 22.2 MB (22158448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067eb0191e16ecf0c10ad1e1131b6a544e172f6924eb7265c34715c3e05dd165`  
		Last Modified: Tue, 14 Oct 2025 18:16:15 GMT  
		Size: 21.6 MB (21626192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584b85e33c6ec61753c205e4cb367af564cd72d841fb5760898fe64a32122dbf`  
		Last Modified: Tue, 14 Oct 2025 18:16:11 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6307e1d8df66aa28d2bfcd0f6b190d5f812d3c4611bc69cc54e6a5c4e51be4cc`  
		Last Modified: Tue, 14 Oct 2025 18:16:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e1e2cbeac74f1006714d0ff16cf9f940746e7899999bc940e66c1d417eacb`  
		Last Modified: Tue, 14 Oct 2025 18:16:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:723a7fc3f5e7aa3e88ae2bbe05306e50524300493a2d8af9ce486add021bd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a23d336fff833419115f69a146756c1ee3ccb8e8e8cfaa7109ab53aec8e875`

```dockerfile
```

-	Layers:
	-	`sha256:d8b5a58aea361248cbe564fea03e6a0c2faeee9ade528733aa93ccfcca9470b2`  
		Last Modified: Tue, 14 Oct 2025 20:08:00 GMT  
		Size: 37.9 KB (37911 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a4471df7b43f9290b85353d85c0a4fa038db1dcb3db281f1963d1f9d9cb70f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70889308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937bbf6f8dc909146785e8d035ecb091be43f6373eac09432ca128b4499eb33a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_VERSION=29.0.0-rc.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 14 Oct 2025 15:11:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb9ca3cf1aac51ff7036ce70f3c442ba8cdca880da0c5a4056aa66562f1b01e`  
		Last Modified: Tue, 14 Oct 2025 18:17:11 GMT  
		Size: 8.1 MB (8113341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5e5673840232357d1f25418a59fb97b76b42f1a425c15d2bc8614bf748393a`  
		Last Modified: Tue, 14 Oct 2025 18:17:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcc269f09c0379a51b11cf127c4b103ab97c0a2be9a12d59cb5fed157185df8`  
		Last Modified: Tue, 14 Oct 2025 18:17:10 GMT  
		Size: 18.1 MB (18139819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03c9ddb6ae363b065134574abe8d374139a9534c199a588d81ea5b0151ee4e9`  
		Last Modified: Tue, 14 Oct 2025 18:17:10 GMT  
		Size: 20.8 MB (20758338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a86dc13998aa8cbef13c09af9363908ea22230a193511e71213689f2aeabc3`  
		Last Modified: Tue, 14 Oct 2025 18:17:15 GMT  
		Size: 20.4 MB (20371577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4015e1d10dd9f79f8fa2e6dd03292c98807d1f38c23b084f304058f376f146b`  
		Last Modified: Tue, 14 Oct 2025 18:17:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce023d26ce609c4a88602f842ffae81e6aef17546999d1357ba07645b870e4ba`  
		Last Modified: Tue, 14 Oct 2025 18:17:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b617f27ab2ba53c7003c0a2fe5c0d14c2399c36a7d1bf12818a0a728e027ab`  
		Last Modified: Tue, 14 Oct 2025 18:17:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ccd9421ade906304e2a5145489b785138d112dc14ef8cbb7f1efde5b2ad19ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb1b4f1bf0a9823b70da0198e7e62a790999fc8f95c4616ad2d818eebfb783`

```dockerfile
```

-	Layers:
	-	`sha256:02d66e523e923f017e2431df62385f7c351a528d2a93096b9f34e290974a6fe8`  
		Last Modified: Tue, 14 Oct 2025 20:08:03 GMT  
		Size: 38.1 KB (38069 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a047f516f95c8e4e23c37e4465c325723914defe0155e25a458dfdcd36865ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69886660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063f54e1867c6045a47614f098ea5efc768b9c0f7f2eb0373a6cf6c2591e511e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_VERSION=29.0.0-rc.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 14 Oct 2025 15:11:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a9e8d24db0bc0df33b4e41506822b46d4e752903438fcdf66bf7e44f23d152`  
		Last Modified: Tue, 14 Oct 2025 18:16:12 GMT  
		Size: 7.4 MB (7437547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495077cfaa254620d03a42273ca1db9575605a588a6592f57d4551d3f617a36e`  
		Last Modified: Tue, 14 Oct 2025 18:16:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f91c0fcc6200dc1923e2289a047cbf72528dd316ad6719d2d74d43b904baff`  
		Last Modified: Tue, 14 Oct 2025 18:16:13 GMT  
		Size: 18.1 MB (18128497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea96f62ef9865052158e0c348a2fe5e0fbda318b805a77294461043e85031f95`  
		Last Modified: Tue, 14 Oct 2025 18:16:13 GMT  
		Size: 20.7 MB (20744390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91205569800440260578032bbae2105b530bb795f47c8ad94b5524a36ed1ed4b`  
		Last Modified: Tue, 14 Oct 2025 18:16:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85892cd9fb9705efadc77976567086480888403e595ef150038d7b0671a0ba73`  
		Last Modified: Tue, 14 Oct 2025 18:16:12 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d38384375ec384ba552a92c350baf2467d404ba8fcb7028ce142cac0b0a88a`  
		Last Modified: Tue, 14 Oct 2025 18:16:12 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cc2d52ed73775d49ed59f3c4c5d6b5d82af0327021cade666f412e96bc7f53`  
		Last Modified: Tue, 14 Oct 2025 18:16:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e5ad2e241ad0bf866ad85e22cf2cb226de6b84d5790df99b54901530856b7b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f2fddbb79a1519afa42ac8cebfbec7f882f6e028b8dfc5d74957dd42639561`

```dockerfile
```

-	Layers:
	-	`sha256:d2efc7c44b391a53dc14c6e39217cda787409bd8f6eaed2e3487ca298e9e7ca6`  
		Last Modified: Tue, 14 Oct 2025 20:08:06 GMT  
		Size: 38.1 KB (38069 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:17b7f88f791b17ab65183040c2aa4db18db2d16813846bdd1f56f9c627a0e828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70652953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dbbc39e2200be56019099dd6596a2606f72338cf2908cf74947baa3d68928e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_VERSION=29.0.0-rc.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 14 Oct 2025 15:11:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b10e0305b1e19fc16fd80eba3c72fc942b09acfdcc0d3540a4e16902fb22952`  
		Last Modified: Tue, 14 Oct 2025 18:17:30 GMT  
		Size: 8.2 MB (8227549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abbe9e2de40ec4b6ec5d0ddaae54a61ccea7854a8e6083ba1896eb1f87c9934`  
		Last Modified: Tue, 14 Oct 2025 18:17:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01990adf97c0b40d144de38838718ee85c7aad6900c0536896ccf67f05fad2af`  
		Last Modified: Tue, 14 Oct 2025 18:17:31 GMT  
		Size: 18.3 MB (18256393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8d87c8051c8128007e5b8de599dae3fdaa21d825458d872a4b7a0aa7a115b3`  
		Last Modified: Tue, 14 Oct 2025 18:17:30 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18e52451505b7e8d643b576eddae489e9f0447778788422e0be149aaa942cc6`  
		Last Modified: Tue, 14 Oct 2025 18:17:31 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6de01507dcde6cc0ad11b4896bd257182b39f0922178cb57f4005be5da3b47`  
		Last Modified: Tue, 14 Oct 2025 18:17:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef632edb75087d839168a9728b8c43422e80e0479f1f95ebd396634e6b6a738`  
		Last Modified: Tue, 14 Oct 2025 18:17:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87dda9dfa6953b97784730f4d512e3afcc6001d0e4875e12b3af4d910957114`  
		Last Modified: Tue, 14 Oct 2025 18:17:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bdf602593f391e327ebccf923cf111d916e79dad48e2d3ab73d237f20c245185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d385e4d9ae80fa4b4e46a7ecb4eba0b335fb8f2206ab6fa10b84dc95db5b5f7d`

```dockerfile
```

-	Layers:
	-	`sha256:260356b50b25c09097ec43764df48bda8c4adb4224c3c29e46e6c96d9b592746`  
		Last Modified: Tue, 14 Oct 2025 20:08:09 GMT  
		Size: 38.1 KB (38105 bytes)  
		MIME: application/vnd.in-toto+json
