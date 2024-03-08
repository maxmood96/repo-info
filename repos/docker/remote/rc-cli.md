## `docker:rc-cli`

```console
$ docker pull docker@sha256:a30eec44267d686088dcebe558bc4a4ee56036943ed4a15a31a9bad08132129e
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

### `docker:rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:b57c095a5f0b0cc33d256c4326c00d6768dbdf0924830e49590a8711ba2a124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58532494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bf12c836a18fb0a681fc4f333adb472e50da46a829b23c78a2c4d2b7a5de08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 18:07:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-amd64'; 			sha256='ddd69ee2ca3dd61760e771dcd2f3453dc677dfeb42c9484cc2321b96bc1b7c57'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v6'; 			sha256='6aea498b2a168bcd13f919e85e0670c2e5a71abab8ecd6bfe52874d14680f617'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v7'; 			sha256='1566b6f3cf69d06ade467d9928e19f6a6682182fe3008bc9a0c83385d5637fa9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm64'; 			sha256='fa36eb4deab2fac6ddf5fdeddcf16999bc9d5fb1d632e0ba7e572b519df8a656'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-ppc64le'; 			sha256='aced23b7832c690703d0cb6339d4ccdbac9b45f0392b865b131aba9b572ae3c1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-riscv64'; 			sha256='c15e51986d59398552b3ecd50b4ca75779e42c878e34761df54616ac02165207'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-s390x'; 			sha256='c3578ab9814e4c2d0f917721b1dfd140b85e40602f6128745178a051cf4d0196'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 06 Mar 2024 18:07:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Mar 2024 18:07:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c70fa28bd47b8c239eb5ca27d77af0f3e6b5b4bf650a64371e0419ded7924d`  
		Last Modified: Thu, 07 Mar 2024 18:49:35 GMT  
		Size: 2.0 MB (2018462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba0502d51f75eb2ea66cc609be7349e3e740ec4cd3faceca46eaa5634b6162a`  
		Last Modified: Thu, 07 Mar 2024 18:49:34 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4baef5582a6338b59d71881630bcce8ce3f907d34e5810ec2441880406205f63`  
		Last Modified: Thu, 07 Mar 2024 18:49:36 GMT  
		Size: 16.9 MB (16906057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233461d18016a0a6c93ffb091d10e1ef06111c13d77500f950b1da0fe9bba40`  
		Last Modified: Thu, 07 Mar 2024 18:49:35 GMT  
		Size: 18.0 MB (17982453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf1dc48541576a54aa37f8529d97a88d860686469b49ed8ffac5e613e7f7df0`  
		Last Modified: Thu, 07 Mar 2024 18:49:36 GMT  
		Size: 18.2 MB (18214532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f65f978ebaf1d5fa25da63b46951536b129465205fccedc3fa453caf9d55a1`  
		Last Modified: Thu, 07 Mar 2024 18:49:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ad4da4b67d48d01078cba113e6b2b406a28647c77fc7cd1c04996b9f7638e3`  
		Last Modified: Thu, 07 Mar 2024 18:49:37 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0afa7b9f090e70420aa605519bd43bb03b6418ba4c400081cdb8228221bbd7`  
		Last Modified: Thu, 07 Mar 2024 18:49:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bef324aaac81992be8aa8f0500f9a231ebd23a2cc1bf263a796574b890a30c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.2 KB (440193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e4772bfa1da482ee67ce602b6b2ba9da5b9ccc7a344ed68f097c672360749f`

```dockerfile
```

-	Layers:
	-	`sha256:1389dfec6bcb0d057ae6304e485c23b69538cbf6eb4b593f152e4992186e4bc9`  
		Last Modified: Thu, 07 Mar 2024 18:49:35 GMT  
		Size: 402.4 KB (402376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929f00f584481aab848ae07054be0e42d696fd9d9227ab5fb30c8f65284a627b`  
		Last Modified: Thu, 07 Mar 2024 18:49:34 GMT  
		Size: 37.8 KB (37817 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:492fa46dd8f587e755f585410b3e55d6ecac05cce3fc414a18433d98e7de35d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa3a32b4256ce31c1b120fdc7ccf4b1b8019d348494b5931c652928834bfeba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b644515427b339d759c0893c759cef3712594a3f94e1032049e20c70b4e2b4`  
		Last Modified: Thu, 29 Feb 2024 23:26:53 GMT  
		Size: 2.1 MB (2108659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648ef94eae9908d98c672a4dd6dc6035976f446aca14300d96f2b66f828e7f52`  
		Last Modified: Thu, 29 Feb 2024 23:26:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516ca0d5ec978deb82d5072316cbb86c5ef37b6f8f8202705b9e3592cde624ae`  
		Last Modified: Thu, 29 Feb 2024 23:26:54 GMT  
		Size: 15.3 MB (15287824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2c3c919ec8fb7a0eab05feb72c9635b13c2dff0050a408cf45f68f484ee901`  
		Last Modified: Thu, 29 Feb 2024 23:26:54 GMT  
		Size: 16.1 MB (16099978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10380a0d25fd7d80ad44fad3f5b6945dc100b907573c8921c1034a4e28f50f81`  
		Last Modified: Thu, 29 Feb 2024 23:26:54 GMT  
		Size: 17.2 MB (17207701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e8d4125ef8699e0f466f81b139004e283429668e66ae320d1da174eaf2f66d`  
		Last Modified: Thu, 29 Feb 2024 23:26:54 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06babee6ea372f1296ff27e8348e0cd91583308cb4c6f799f5a5e915d362c089`  
		Last Modified: Thu, 29 Feb 2024 23:26:55 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0de69755a40dbf13c341a4d448b9b7ae721073e0f4f4aef9ba2c4cd0e475c6`  
		Last Modified: Thu, 29 Feb 2024 23:26:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:695c9d8247261a79a1b54ab0c0e641e2252adbb50dfaa893afbd75f1934f9b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac1529fa8e622c102c0001bf09b64e81373dde00b373c311aa8934e9d47478e`

```dockerfile
```

-	Layers:
	-	`sha256:7a1268b3ef6af21f10a86e5aacfa999a836d6a2f9dfed1f83887767c375af339`  
		Last Modified: Thu, 29 Feb 2024 23:26:52 GMT  
		Size: 37.6 KB (37585 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:d5b97363679012942939cf0bbe741ef112f6359e14083bf74de01b11ec583d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54102197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc95f7fcc6ec4f090c6919e645ee7f0b99d5d14e7a86e991c2f9baeee2aa6081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 18:07:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-amd64'; 			sha256='ddd69ee2ca3dd61760e771dcd2f3453dc677dfeb42c9484cc2321b96bc1b7c57'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v6'; 			sha256='6aea498b2a168bcd13f919e85e0670c2e5a71abab8ecd6bfe52874d14680f617'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v7'; 			sha256='1566b6f3cf69d06ade467d9928e19f6a6682182fe3008bc9a0c83385d5637fa9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm64'; 			sha256='fa36eb4deab2fac6ddf5fdeddcf16999bc9d5fb1d632e0ba7e572b519df8a656'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-ppc64le'; 			sha256='aced23b7832c690703d0cb6339d4ccdbac9b45f0392b865b131aba9b572ae3c1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-riscv64'; 			sha256='c15e51986d59398552b3ecd50b4ca75779e42c878e34761df54616ac02165207'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-s390x'; 			sha256='c3578ab9814e4c2d0f917721b1dfd140b85e40602f6128745178a051cf4d0196'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 06 Mar 2024 18:07:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Mar 2024 18:07:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12baa34c4b3af0d924c08f5c0364298070ad555de60b11bb8b9d270e51fd6ad0`  
		Last Modified: Thu, 07 Mar 2024 18:50:35 GMT  
		Size: 1.9 MB (1896140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce178a6d07ef665083e0bb7a5011401991ac2ce60e1dd3674325bffe854ab5b1`  
		Last Modified: Thu, 07 Mar 2024 18:50:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aae121f4c6e463c253ea668f964dd5d7d26343756d552167d75ce8a755788e6`  
		Last Modified: Thu, 07 Mar 2024 18:50:36 GMT  
		Size: 15.3 MB (15276517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538317b0a451c98b29c279b1a9dd9bfa7159c3f358c7f9ae0c7d50fdf815fa7`  
		Last Modified: Thu, 07 Mar 2024 18:50:36 GMT  
		Size: 16.8 MB (16804267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c800e1fddcc64412702ff8067e7f649317cd262cb90e289e6e3c06c964f2d17`  
		Last Modified: Thu, 07 Mar 2024 18:50:37 GMT  
		Size: 17.2 MB (17204117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f339ab4d0aede8ce7731d0f324723b5ba0268ab2c3c598bd7a88a9dee4bfd5`  
		Last Modified: Thu, 07 Mar 2024 18:50:36 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fdf6a4e48f6f4f82e74aa36048a51f78a1d53681d16789d00483fc7f40125b`  
		Last Modified: Thu, 07 Mar 2024 18:50:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebaa99ef89d54676785aa2263f4fc4b7bb3486655eac4ba196e8273c83786c8`  
		Last Modified: Thu, 07 Mar 2024 18:50:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c250123e1581aeb3aa2d9cc6f29e0cef12aa2144fb3d80efca15b88028fddc11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.1 KB (440103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396b34b5161420ae185e2bc060021cda4e5ec073f64c73343a7582cd12cb51b9`

```dockerfile
```

-	Layers:
	-	`sha256:61000cad0fb399f384d8f29f08545ee6eb79260d4f6a0850a84fe07431e814b0`  
		Last Modified: Thu, 07 Mar 2024 18:50:35 GMT  
		Size: 402.3 KB (402304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790f545ff61baf8ae1c9b85e0bb42aaa1786f8892709a8ce9226d111a9760d37`  
		Last Modified: Thu, 07 Mar 2024 18:50:35 GMT  
		Size: 37.8 KB (37799 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8a687d06c65a89c27462326b18aad253fcde48201d8571e0db6a701fa9e8a5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54279121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7dd485204eb0ab7d6cc8ef4443fe2db9d77ddf71527107a09b774ddee709d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 18:07:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-amd64'; 			sha256='ddd69ee2ca3dd61760e771dcd2f3453dc677dfeb42c9484cc2321b96bc1b7c57'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v6'; 			sha256='6aea498b2a168bcd13f919e85e0670c2e5a71abab8ecd6bfe52874d14680f617'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v7'; 			sha256='1566b6f3cf69d06ade467d9928e19f6a6682182fe3008bc9a0c83385d5637fa9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm64'; 			sha256='fa36eb4deab2fac6ddf5fdeddcf16999bc9d5fb1d632e0ba7e572b519df8a656'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-ppc64le'; 			sha256='aced23b7832c690703d0cb6339d4ccdbac9b45f0392b865b131aba9b572ae3c1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-riscv64'; 			sha256='c15e51986d59398552b3ecd50b4ca75779e42c878e34761df54616ac02165207'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-s390x'; 			sha256='c3578ab9814e4c2d0f917721b1dfd140b85e40602f6128745178a051cf4d0196'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Wed, 06 Mar 2024 18:07:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 06 Mar 2024 18:07:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 06 Mar 2024 18:07:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Mar 2024 18:07:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1445a503f72c73d6089a1119111ac23a281bc485cb856ca4679fe872c1a9ac8f`  
		Last Modified: Thu, 07 Mar 2024 18:50:58 GMT  
		Size: 2.0 MB (2019674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15768397550ab4bff548e50cb3f24c0a65a8e000b6e0f00a9930bd55c3889118`  
		Last Modified: Thu, 07 Mar 2024 18:50:57 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdacb8f78c96eb268607e8d7bc76eb613ac6bfce9a600feeb7b417773696ffa`  
		Last Modified: Thu, 07 Mar 2024 18:50:58 GMT  
		Size: 15.9 MB (15917018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f16c6640db4ea0d7c78c46224f2f420a0d85cdb4b40d004b157632cc3101120`  
		Last Modified: Thu, 07 Mar 2024 18:50:58 GMT  
		Size: 16.3 MB (16349453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728b69657f2a73dfe9f024df6161681730f62aac02f280de0eeda8d08e2d239c`  
		Last Modified: Thu, 07 Mar 2024 18:50:59 GMT  
		Size: 16.6 MB (16643002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c2f6321aabb908945ad9ab41cb190ab1074ab40f46cfdd7fecf655db8362d1`  
		Last Modified: Thu, 07 Mar 2024 18:50:59 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52b3819e09c50eb66ed95417cf1415cbf1c0748ef6ce67332779505755b8b8c`  
		Last Modified: Thu, 07 Mar 2024 18:50:59 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2d00ba44f3456838a7dba2ce88ada9a6d38cb3b3755a887ff2fc53af61c756`  
		Last Modified: Thu, 07 Mar 2024 18:51:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:87631ad3cfb17bcf506ed405a726778c03767ea03afd02586d105a974cc601f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.0 KB (440049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262eba92070726273768e3bddcb1fd1707b6dfcea9d46466152b02f7c1cc0719`

```dockerfile
```

-	Layers:
	-	`sha256:7cfdc5642f7561061059eb3fa0071c7669020656b1ba8e2e285eab7f6a8af7ea`  
		Last Modified: Thu, 07 Mar 2024 18:50:57 GMT  
		Size: 402.4 KB (402387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762fd919110bdde8ee564e89aa0b225b27952b4d845fc6695d0a3f4d28a85a47`  
		Last Modified: Thu, 07 Mar 2024 18:50:57 GMT  
		Size: 37.7 KB (37662 bytes)  
		MIME: application/vnd.in-toto+json
