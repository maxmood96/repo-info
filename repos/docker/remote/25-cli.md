## `docker:25-cli`

```console
$ docker pull docker@sha256:2830d5bd946eda9c6c7b4977e851d247baac2bd240bec9fa81eede399b4ead0d
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

### `docker:25-cli` - linux; amd64

```console
$ docker pull docker@sha256:b47d7cf60b365e4ebacd73583b8f481a81e4bf66a8376e1453df8ba230a923e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65619660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536d510396ad4e17b5317d5e2b765b989e8f8c218616589f03f1b318654dc8c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:06:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jul 2024 17:06:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:06:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1abce3777b950e78d4a72e4139982f856c6ea7cfb6dfa7f9cd7eadf4b70de70`  
		Last Modified: Thu, 18 Jul 2024 18:55:33 GMT  
		Size: 7.9 MB (7869247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b516da8ddbbcf9302b53fdfdd299ba7b61fe9fdc69c3da7808ff8c4f4a29e`  
		Last Modified: Thu, 18 Jul 2024 18:55:32 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf6e9d12b8a18a6bb848251716529f40451c4c2a008406cf292f97e2e2297dc`  
		Last Modified: Thu, 18 Jul 2024 18:55:33 GMT  
		Size: 16.9 MB (16902834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3ad476cbf4e947d99a7c28850efd301dbe3240b17f5cb058a40113a2392f2b`  
		Last Modified: Thu, 18 Jul 2024 18:55:34 GMT  
		Size: 18.4 MB (18404632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4ad1ffb30b447cf08397a3597640295c17ebbeb631891b91257ba9c948894`  
		Last Modified: Thu, 18 Jul 2024 18:55:34 GMT  
		Size: 18.8 MB (18816953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9da557f11c19d683db66e499195b102f5105e6ba49f59d3934466fd64b0a20`  
		Last Modified: Thu, 18 Jul 2024 18:55:35 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fb8c7e17ab02b5fa1c05bbe904db38bcfdb954168b15a4ffe1c21d009d2dac`  
		Last Modified: Thu, 18 Jul 2024 18:55:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4741f47e6de7f380049ea41d293c726fc2f36d9777375ab1ae1905c8e3109b`  
		Last Modified: Thu, 18 Jul 2024 18:55:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:89072e81086b9535a8bebb46b1408ca1dea6fe2cf3edc27e0d6bd0021a5d5ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c2b5c72fe65fe23699443644f2d7aa8f5648e7a9ee0e38aeeaf4dd9a0bacff`

```dockerfile
```

-	Layers:
	-	`sha256:9d0fe7da349e80b5379d8a0f7ad471540f1cf5f70f5c89183614fef6237d23ed`  
		Last Modified: Thu, 18 Jul 2024 18:55:33 GMT  
		Size: 37.6 KB (37623 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc6116fb64e7f058b9b909dcb17efe3055daae859255ce7a3b2ce0bb45c97fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61333497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5b19f89ad3f2b803d0b9a2844dbc08de4ef8c85a65c41c063a52f72b450b04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:06:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jul 2024 17:06:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:06:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e10c9bca22e7ab6aaea6bdc57330899ade38e16a894f9dccab4514ceaa4d4e`  
		Last Modified: Thu, 18 Jul 2024 18:55:12 GMT  
		Size: 7.8 MB (7799521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0826832a4ad2b630a8812ec7da2e09e37c6b4aafaa413b8bee895a4d133d744`  
		Last Modified: Thu, 18 Jul 2024 18:55:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d3c170fc259e91f706db1de9d56c813b635102223b668ed3547e378246f881`  
		Last Modified: Thu, 18 Jul 2024 18:56:15 GMT  
		Size: 15.3 MB (15274085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79852b835b44cab132897686ed5e70557ca9d406e493547a4234409423dab6d0`  
		Last Modified: Thu, 18 Jul 2024 18:56:15 GMT  
		Size: 17.1 MB (17117107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655bfdb424463a4fac47629d755193cb3e03f6c24a79f105a206d9142f2c162d`  
		Last Modified: Thu, 18 Jul 2024 18:56:15 GMT  
		Size: 17.8 MB (17773479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cce964f9145b29463f3a2712a2b2204bccf4edfa9b6b34db8f49ccaa2a8146`  
		Last Modified: Thu, 18 Jul 2024 18:56:14 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202e0b1ae7c633849496c0d59b102ffc19b1eb52f4e9d5e4c8250f0b02b7554e`  
		Last Modified: Thu, 18 Jul 2024 18:56:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc393a1bde8306f0b7b94792149401f1007265e91d4945cee541a984cdb4936d`  
		Last Modified: Thu, 18 Jul 2024 18:56:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6731ee7b722194ff9c61243fb7ab5d0676a819ff260e07158efcc7fba186a26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846d1419af1a4bff1b3e0a7946c32db44f458e5a08ef2358600d6f8eb2c05f6`

```dockerfile
```

-	Layers:
	-	`sha256:963d033c4c4e7f39884e87a03be00a7ed536b377d9d77a0c9703c31010c248f5`  
		Last Modified: Thu, 18 Jul 2024 18:56:14 GMT  
		Size: 37.8 KB (37770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:7776b97e190bc4491a147a51140c560e1fb83af5f27e37521b8bd82104570532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60373823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e59db67745f6a761cb6fabb4b4a7ca92f6fe537483bd9edc350fb533281fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:06:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jul 2024 17:06:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:06:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f9c1cb3f348935ccc2213b45a6f967fb9ef04e90990caa00fa3a8df1888bc1`  
		Last Modified: Thu, 18 Jul 2024 18:55:14 GMT  
		Size: 7.1 MB (7138017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179c5d549bc55c8b6f2281001fff6db882e560d7da01693827da1c931a9a8692`  
		Last Modified: Thu, 18 Jul 2024 18:55:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88de88bf34706b512698d776f9dadd81bd9410cc87eed0b3ae004fccf85cbe0`  
		Last Modified: Thu, 18 Jul 2024 18:56:13 GMT  
		Size: 15.3 MB (15273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bde1c86866321272a39ca557daabc0fb77ce37de97887cf2a07351557f0859c`  
		Last Modified: Thu, 18 Jul 2024 18:56:13 GMT  
		Size: 17.1 MB (17104571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddffd6536aaa840f6d17e1de2f2db2b5aba3cdf0c0d9baee14c4b51825b1e459`  
		Last Modified: Thu, 18 Jul 2024 18:56:13 GMT  
		Size: 17.8 MB (17761054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472d2121f4769b0de3770c89ee1717ee1363627d48e02ebadd13153bbd9ff287`  
		Last Modified: Thu, 18 Jul 2024 18:56:12 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea5f304fa0e7d9f331c5926adc8d0a2c763b66a911acc85f6792f6344f3bcfa`  
		Last Modified: Thu, 18 Jul 2024 18:56:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4bdbed62f9735c61a867e21f016606e5ba2675b327bbdead054ec371aa94b3`  
		Last Modified: Thu, 18 Jul 2024 18:56:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:239945cf626c395d40f239ebb5b13a6b0b9fa6bb01ca1b5db20acfb0cf77c2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbb83a503e902b8f5ec10f132eda37ca478887da65e67c8a6831fa8ade45201`

```dockerfile
```

-	Layers:
	-	`sha256:e47abf9a20fec419fabe7f93c9ee3f873d7860c8190738ec1c6ad643cb5f69cd`  
		Last Modified: Thu, 18 Jul 2024 18:56:12 GMT  
		Size: 37.8 KB (37771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f867e770406887aa7c09639dd8f024f282e362f74cda36ea1947dbf16803afd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61921923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ae2955f6432ac895c6842e65fcb7cfef905477289e9dfc8674d99a32376706`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:06:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 17 Jul 2024 17:06:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jul 2024 17:06:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jul 2024 17:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:06:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2649985fe95ea7b64683a03a22cda12e6203403323506a2605bda4c9ad56ec1f`  
		Last Modified: Thu, 18 Jul 2024 18:57:02 GMT  
		Size: 8.0 MB (7974739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69fb4b09a403c091ca2d24994a101bc49383215888dcbd2752c99875fc041f5`  
		Last Modified: Thu, 18 Jul 2024 18:57:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a22fdff5577937df185e0f70b6c7d7e2f07187744daf745e80fbc3e8a0172e1`  
		Last Modified: Thu, 18 Jul 2024 18:57:54 GMT  
		Size: 15.9 MB (15907335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dbb2f0855c30108ff5aecb356b71bfebb83cb5fc264f5711d23c9f288de2eb`  
		Last Modified: Thu, 18 Jul 2024 18:57:54 GMT  
		Size: 16.8 MB (16772847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcdf6228b676dd893ac3607415983d5f6fedaf3dd619e766be34b743759c820`  
		Last Modified: Thu, 18 Jul 2024 18:57:54 GMT  
		Size: 17.2 MB (17176047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cfb934bf26df6018032726951a16e898f2155e2320ec7df9d70be53ccd2636`  
		Last Modified: Thu, 18 Jul 2024 18:57:53 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7419c6cef5b36eb79ead29e3bfa355f7a9ce70f83cff110434ad476429d25f02`  
		Last Modified: Thu, 18 Jul 2024 18:57:54 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0449341aab0c999e02b974fbda5ff4ef49435a776928fef7c1d7bf448b50c4fb`  
		Last Modified: Thu, 18 Jul 2024 18:57:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:80bf571e69a45b7dac2a434d4697c3ec635391c8632e52ba12bd1ad768ed4f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c04d8e470df3c9a489afab68077b89156e528227490dc6c0928bae0c7703ab3`

```dockerfile
```

-	Layers:
	-	`sha256:166c32d714b0f0b974fabe60ce5c1b0bc68e6a71896bfab11989c2d521f027a4`  
		Last Modified: Thu, 18 Jul 2024 18:57:53 GMT  
		Size: 37.9 KB (37920 bytes)  
		MIME: application/vnd.in-toto+json
