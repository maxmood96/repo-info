## `docker:cli`

```console
$ docker pull docker@sha256:ce0e841c236b1f68d38300da1775c34bbe16915fa053d94efa37dd073a9957c0
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
$ docker pull docker@sha256:2ddfc275d5d1c4821b063db1c2f1f53da167a9ae54a426a6d2cffeea2b598b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66786659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fccb4dbaabe6b56e80380e061aa85328dc468f34363086307d691b0e297ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:10:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_VERSION=27.0.3
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jul 2024 17:10:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:10:28 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc205cab7dabb6d1b80868157a306f2894d909926a0507d162e166efd15aa4a5`  
		Last Modified: Thu, 18 Jul 2024 18:55:23 GMT  
		Size: 7.9 MB (7869296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1847eeb0276f28ed3e9c263a78be14f06d1060865ab65dcdc1ac923fb8c690`  
		Last Modified: Thu, 18 Jul 2024 18:55:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c20a579481d6c36174aadbda2308dda4d49daa4cc57430409ba17cb6e1990ed`  
		Last Modified: Thu, 18 Jul 2024 18:55:23 GMT  
		Size: 18.1 MB (18069808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d05d4bc6becfdcf9d1ed1b3475e76088a74ba16d6d89952613903422a169ea`  
		Last Modified: Thu, 18 Jul 2024 18:55:23 GMT  
		Size: 18.4 MB (18404605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7d6f122253b107485a03bdb9783267ee197d88ae51494a62baca94a6113edc`  
		Last Modified: Thu, 18 Jul 2024 18:55:24 GMT  
		Size: 18.8 MB (18816953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20e62ad61f04ca133f18b58745a62a6f3354405821779790dc49ce11d42c90c`  
		Last Modified: Thu, 18 Jul 2024 18:55:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29152ed7fd0f9ca7a0997de5f9dedb9ae6461ba5b17673209f9b2e6a4bcdf58d`  
		Last Modified: Thu, 18 Jul 2024 18:55:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88c12977ec62e9c0564ae104cb6409665eb211e5281f920635ff8d46457e21`  
		Last Modified: Thu, 18 Jul 2024 18:55:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:26074715824d96abed44358dabfc4713bc7e14f07e4432eac3bb94342c15e2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4acc182ca4929384362999605867479cdff392d443429c8ce1f0389dddd5fdb`

```dockerfile
```

-	Layers:
	-	`sha256:8a52cb340c1e902630477e59b5c3b887099310ca8f9f00e4e65bbaf89c93d7e4`  
		Last Modified: Thu, 18 Jul 2024 18:55:22 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:737cbb00a8d2bb25fa8b4b56a5039720f60883fc95b351a61be410f0ee318dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62404918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6ace3168794884a08378512f752903f2e9095ba778af085765e1336cb4adc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:10:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_VERSION=27.0.3
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jul 2024 17:10:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:10:28 GMT
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
	-	`sha256:454fbd0244d77bb08b64c1208f8d549c50f1184c43999dfa4d4a7861ce7ea8b0`  
		Last Modified: Thu, 18 Jul 2024 18:55:13 GMT  
		Size: 16.3 MB (16345542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18506adbe8475eeb772251a8d92b79b73c1ba86c872f5286dda1cae575528518`  
		Last Modified: Thu, 18 Jul 2024 18:55:13 GMT  
		Size: 17.1 MB (17117082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658b7b9cdc36313226b0df107ae6c1d8d297e5cf4346943909397b916e9aa0cb`  
		Last Modified: Thu, 18 Jul 2024 18:55:14 GMT  
		Size: 17.8 MB (17773473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de792a0fd85d87c2fff200e02d5d5cc38a1d4d3e88531e0e62e41fabe9c7e82f`  
		Last Modified: Thu, 18 Jul 2024 18:55:14 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fa5a882beab76a5f08e7a26950cb9e49cf67a4b789b055fa14e9c692332b0c`  
		Last Modified: Thu, 18 Jul 2024 18:55:14 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61469f5d79120f54dd09aeed666cd228c6be2bb78eb95db8f27a12552f05924`  
		Last Modified: Thu, 18 Jul 2024 18:55:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:59b8de8ba24bcdf70fa469286c98296b7da3939e27df52bd94d7ac58721d931d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcfd2310251d25d66ea719e190a90e45cca3b6e7f2318008d6c9ccf103c3d59`

```dockerfile
```

-	Layers:
	-	`sha256:f204760d23c41642a7fb1fd403fcbd15e7b504cad705632516a7568e41658f89`  
		Last Modified: Thu, 18 Jul 2024 18:55:12 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:8e681b6284e121f35e8ea422fe09582fb3f8b776b4bdb68fc5b1e500ed39f900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61439821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c151a88c92c4c2113c04ad2b726047119cd0ccef324ecd919100806177efb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:10:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_VERSION=27.0.3
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jul 2024 17:10:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:10:28 GMT
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
	-	`sha256:fc217adeb8d73e1a9249d02bdf545c0cdbdf0bd724977915c606553d200ebcaf`  
		Last Modified: Thu, 18 Jul 2024 18:55:15 GMT  
		Size: 16.3 MB (16339186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045cd8a39abe3685c067e790ebd9e3c7523d7b626b1718a2c93a70af6a8f09bf`  
		Last Modified: Thu, 18 Jul 2024 18:55:15 GMT  
		Size: 17.1 MB (17104562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd092009fa074fd05bf2bba3ed8749c17abb1d0de9a8a879c7e165bde664c20`  
		Last Modified: Thu, 18 Jul 2024 18:55:15 GMT  
		Size: 17.8 MB (17761046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c448dded4bc6492dc405496ea50c9147b66ae35fbebeedce242e4df1d5308b43`  
		Last Modified: Thu, 18 Jul 2024 18:55:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a32336b2529223edcf6389e51243de0fefb90f89431ba22a2afe7fd52f920b`  
		Last Modified: Thu, 18 Jul 2024 18:55:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae849fa5bd79420c307fa2ed9857a222773d73145d1e7c93a85a20fb5b700e`  
		Last Modified: Thu, 18 Jul 2024 18:55:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:7ffed249e415eb4b5ea77dc05d79512330d34433e832d8c321b72c1aac0cccb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106af016ab1b096e620fbe80d5da6424d60fde85238a92fe331ecb20e40306c9`

```dockerfile
```

-	Layers:
	-	`sha256:1059a244f6fdd0931e8b2908b50fb3afa51a94ce0ce77029887aa9eb61145a6e`  
		Last Modified: Thu, 18 Jul 2024 18:55:14 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:91939059231cd9416e119230151b3aa25f9ef0439f8779131fd9061b6ff46d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63043188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d98a230222a15def31e543c4b38188cb15b57226de77d353cb84d87857dfce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:10:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_VERSION=27.0.3
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 17 Jul 2024 17:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jul 2024 17:10:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jul 2024 17:10:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:10:28 GMT
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
	-	`sha256:1c88eb84e2d7256c8b8e1d0553776d90243a05c06711507817c708f13f96738d`  
		Last Modified: Thu, 18 Jul 2024 18:57:02 GMT  
		Size: 17.0 MB (17028616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2fc95335a70f70bf04530ed6321de63f5c56e99937306967a67a8e7571d99e`  
		Last Modified: Thu, 18 Jul 2024 18:57:02 GMT  
		Size: 16.8 MB (16772841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e842971f67e2362316c68cd0bb2da89ba994a63d2068555c01d88753d3d5c8`  
		Last Modified: Thu, 18 Jul 2024 18:57:03 GMT  
		Size: 17.2 MB (17176039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358f5d7c7199465ed20bb662ed738ef00e789061fced25842ac2af29116a9847`  
		Last Modified: Thu, 18 Jul 2024 18:57:03 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19a53c6e2a7a1c4194974b68c31a3e65fab364065d5d956093f7c39727c13ab`  
		Last Modified: Thu, 18 Jul 2024 18:57:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa34ff7d1ccb40b1cae26b9b4511586c675a36c34ff61b9d9c4eb7125bfdbb0`  
		Last Modified: Thu, 18 Jul 2024 18:57:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:cbe90c49167e5e7aa3af24eafd9db1367f5415fd0feee3b8d04864d52e8ff472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f199d28b59edd702f996274350a4a55c4ad8081951d19d9e6dd0ac09dcc6760`

```dockerfile
```

-	Layers:
	-	`sha256:c1bfabdf51c93d12460beffb032f7db8def2c0b69ab754faadda3d191bc1ff25`  
		Last Modified: Thu, 18 Jul 2024 18:57:01 GMT  
		Size: 38.2 KB (38226 bytes)  
		MIME: application/vnd.in-toto+json
