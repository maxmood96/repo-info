## `docker:cli`

```console
$ docker pull docker@sha256:51e23845f5caff1e688a2fae003b0c69d635c9200ad544731db1593731df1d3a
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
$ docker pull docker@sha256:bd856b0b9684b059ef942f0bfe9f3c4246358637a778c29e66e4e74e995ed606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65549813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84c9c005f1015809c1a270f4197d6ccbee67bf385237434b0b5cf6b0122ff5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:32:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 08 May 2026 16:32:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 08 May 2026 16:32:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 08 May 2026 16:32:42 GMT
ENV DOCKER_VERSION=29.4.3
# Fri, 08 May 2026 16:32:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 08 May 2026 16:32:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 08 May 2026 16:32:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 08 May 2026 16:32:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 08 May 2026 16:32:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 08 May 2026 16:32:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 08 May 2026 16:32:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:32:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 08 May 2026 16:32:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 08 May 2026 16:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 16:32:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec23f98706aac7e78b99c5b57b1d75dec972dc79e3cacb916008f5d259aca1b`  
		Last Modified: Fri, 08 May 2026 16:32:50 GMT  
		Size: 8.4 MB (8390731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7913368a8c343e6c02c1adc847d8ec4459c10ca74d84a02703534599755e9f`  
		Last Modified: Fri, 08 May 2026 16:32:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a39f9ce9fa01d9f5397b1525f5e98a4d194e5ed65e85975d9b53425850f8009`  
		Last Modified: Fri, 08 May 2026 16:32:51 GMT  
		Size: 19.5 MB (19509764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdeda4e8c23988183983267fb1d9a88bb98e57eea25cd560e115091e0948d6c`  
		Last Modified: Fri, 08 May 2026 16:32:51 GMT  
		Size: 22.5 MB (22539224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1ff822b384d96d4595f7602097dec335b2acd5bc7676a8b940eafb0e1a7113`  
		Last Modified: Fri, 08 May 2026 16:32:52 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8578dbbf77b05f05c350ab61478118d90b33c33902ad5163a6eab6c9683129`  
		Last Modified: Fri, 08 May 2026 16:32:52 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67445366368bdf201719c21a984723732a1db81a14b254b1892415df7615ec5`  
		Last Modified: Fri, 08 May 2026 16:32:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee432c7809941439a94004d27e82a570ef307a339bb98d5b95170c5f41836e4`  
		Last Modified: Fri, 08 May 2026 16:32:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:709b822377d8dded20e0c6f4f66b88b58b4b26c567ca4cddb004d8e619a28685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffab9865403a896109849ae0fef2b3449a6a71c4b7310a3765dc9b041817f733`

```dockerfile
```

-	Layers:
	-	`sha256:029ddb2fdb02a7ea73e05424e9fbf6a9432b5ec72cd9e8fb9d1a90bc13a9dc10`  
		Last Modified: Fri, 08 May 2026 16:32:50 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:adbc30f137d40d6379f22bf5f5c9d26e943ff8084bd29b78bdeb4f36055340d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61831164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414e035b976a00e778ac88f1d48f56a85dbb2d25d2e77b2fefa89750febdaddb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:26:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 08 May 2026 16:26:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 08 May 2026 16:26:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 08 May 2026 16:26:34 GMT
ENV DOCKER_VERSION=29.4.3
# Fri, 08 May 2026 16:26:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 08 May 2026 16:26:34 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 08 May 2026 16:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 08 May 2026 16:26:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 08 May 2026 16:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 08 May 2026 16:26:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 08 May 2026 16:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:26:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 08 May 2026 16:26:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 08 May 2026 16:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 16:26:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc907a82d85b82de2a7513eaa18bb01b1fb0597805de52b81246030013a081`  
		Last Modified: Fri, 08 May 2026 16:26:45 GMT  
		Size: 8.3 MB (8297561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7475c6307074bcfeb97b20c4926ee15c03e6ef2e6397074db849d7f6654e5`  
		Last Modified: Fri, 08 May 2026 16:26:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0941ec40108b8d76cda50638bdf37ab13b769ea2cdcecf8f77c39e941d5196ce`  
		Last Modified: Fri, 08 May 2026 16:26:45 GMT  
		Size: 18.2 MB (18156878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a1d862d418f88454fbbdc5d93d8be51ee24dab0819e951953ab33b2e178a00`  
		Last Modified: Fri, 08 May 2026 16:26:45 GMT  
		Size: 21.2 MB (21151870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6160070d5a5f62417baf260ac623da00a9be21bc4b0a34c66c545fb45a745fe`  
		Last Modified: Fri, 08 May 2026 16:26:45 GMT  
		Size: 10.7 MB (10650841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60affd47afccc19b6349249dfc6e39211cba5bc2c849470c6369a7ff1f84d5b7`  
		Last Modified: Fri, 08 May 2026 16:26:46 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca78a93024650038466a24ad698f291cb11bb44163960a700c7c5a9f005bab1`  
		Last Modified: Fri, 08 May 2026 16:26:47 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f725bc46cd3373a503bfdffc0c1b82a6f52872e6900d987905310dfca71c7`  
		Last Modified: Fri, 08 May 2026 16:26:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4ea6d0e973e60d484ba6b38d694eca4a46d7098d76dbb5b4f15858395ad20fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647f6ba8de30849c146a43f38981f3a297f1d310ee0995953aff99bc8adcc6a6`

```dockerfile
```

-	Layers:
	-	`sha256:df27c75e9103616aeca699c8f5a2a7bdc70c5a4af85d79a2ba1300e7588c06d1`  
		Last Modified: Fri, 08 May 2026 16:26:44 GMT  
		Size: 38.2 KB (38221 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:245cb889d746ccebdb4c7e6fa66de7d9f355aedd95d61d4b080d098a3a278ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60788036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d6e170c0bdfdd7614fa741469a782679d7c2bed823c2e069bdb3c960d7739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:26:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 08 May 2026 16:26:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 08 May 2026 16:26:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 08 May 2026 16:26:33 GMT
ENV DOCKER_VERSION=29.4.3
# Fri, 08 May 2026 16:26:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 08 May 2026 16:26:33 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 08 May 2026 16:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 08 May 2026 16:26:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 08 May 2026 16:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 08 May 2026 16:26:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 08 May 2026 16:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:26:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 08 May 2026 16:26:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 08 May 2026 16:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 16:26:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e7bbc8fafb104edec52b740ee9247094dac19af02b35a41ef2b5e03bee0a2d`  
		Last Modified: Fri, 08 May 2026 16:26:44 GMT  
		Size: 7.6 MB (7595549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7475c6307074bcfeb97b20c4926ee15c03e6ef2e6397074db849d7f6654e5`  
		Last Modified: Fri, 08 May 2026 16:26:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfddc97c3640f0f7e8ed79b130d4f543a43a8b8bc218960ca554ee7c181e282`  
		Last Modified: Fri, 08 May 2026 16:26:45 GMT  
		Size: 18.1 MB (18140313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8530d1a8c9dfa5a8b4c76147c22f8d86d5ba668f1d9bca6a2fec5450d990cc30`  
		Last Modified: Fri, 08 May 2026 16:26:45 GMT  
		Size: 21.1 MB (21129757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692ebf64a2e7763086720b9b8d459d6e8d632cedf20166715d4db1c561cdc3f`  
		Last Modified: Fri, 08 May 2026 16:26:45 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa0e69097267d224033f6689374b089c35a9c05ce3835054ffaa20ad934bfd7`  
		Last Modified: Fri, 08 May 2026 16:26:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc93f20bd6077d8b074d29ffce1bc6e52b0ee03971795a1ed9c9b1b132335827`  
		Last Modified: Fri, 08 May 2026 16:26:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f725bc46cd3373a503bfdffc0c1b82a6f52872e6900d987905310dfca71c7`  
		Last Modified: Fri, 08 May 2026 16:26:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:00f315b072d13abf2d2515b5f3c85d0023ccdfdee9f1997a1d28ded97ddbc91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9839bf0c51ce2b79d727f8f671e64b7d9f54a77641550418f64f830d6d7a530`

```dockerfile
```

-	Layers:
	-	`sha256:f94e562ccc91d86d4c1d596e3b469b06bcd14b36dddfc3614431eb57919d56bf`  
		Last Modified: Fri, 08 May 2026 16:26:44 GMT  
		Size: 38.2 KB (38221 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:123027172e3a9aa0dd5b5b622c58fa62b187c071c8e0f32da25229074ca457d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61318053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df869a64964c84a569f418f09fa5850e2f47cd4e6af9104143f105769259ad7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:30:58 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 08 May 2026 16:30:58 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 08 May 2026 16:30:58 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 08 May 2026 16:31:00 GMT
ENV DOCKER_VERSION=29.4.3
# Fri, 08 May 2026 16:31:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 08 May 2026 16:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 08 May 2026 16:31:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 08 May 2026 16:31:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 08 May 2026 16:31:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 08 May 2026 16:31:02 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 08 May 2026 16:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:31:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 08 May 2026 16:31:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 08 May 2026 16:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 16:31:02 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16557002e3f9c0f12daad3cf2aa0eeb951785238e78f649fe1a33be164ee3cd`  
		Last Modified: Fri, 08 May 2026 16:31:08 GMT  
		Size: 8.5 MB (8450503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba2f25b8074cba3c42ab763faf8c1eec97f0f1268e18221c315fd39a71cfbc`  
		Last Modified: Fri, 08 May 2026 16:31:07 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0d50d3cbd05ec2ff1d935bcb728e2c0906b010fa46bec38094653add3d6fa`  
		Last Modified: Fri, 08 May 2026 16:31:08 GMT  
		Size: 18.0 MB (17969147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d520c49f69c93efe2c8a5a65659a79b0627ebde2251cc670896e5ee2fbbf9bb`  
		Last Modified: Fri, 08 May 2026 16:31:08 GMT  
		Size: 20.5 MB (20453109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873efcc71ab19d6817bcd802ce087ef621ee9d76ef00ccba44a47ea3b2312b2`  
		Last Modified: Fri, 08 May 2026 16:31:09 GMT  
		Size: 10.2 MB (10243273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11571ea79227e8cd2b7926c36cd8148f1a6566edd6cab24a2f56b91ea6534a3`  
		Last Modified: Fri, 08 May 2026 16:31:09 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a0b06ba0679ee8b78ca3c2dd121c5e7e2dccb9e4ec1eb19c8e9522d1583b20`  
		Last Modified: Fri, 08 May 2026 16:31:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc867a92a4a00d8508b93d50da952ca51038d284ade22fd6e0589b2513306b79`  
		Last Modified: Fri, 08 May 2026 16:31:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:ebe68452cc8cc3ef8a27c292861eeae0040906dfdb02591df9e6c40486e510e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3edd3693cf5ac6600d4c280f7598e80d697606387cd1de6f52b7fba6244cb36`

```dockerfile
```

-	Layers:
	-	`sha256:864c5c9cdf4692a97346899edbb6f48a7fc59b108289f8352235d4c4f2141bc2`  
		Last Modified: Fri, 08 May 2026 16:31:07 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json
