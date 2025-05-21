## `docker:28-rc-cli`

```console
$ docker pull docker@sha256:8212316d2e16cdc35adb6359f39514a9ac1853cf36d0d0aad889c7ee476b14d6
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

### `docker:28-rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:0f75fb7efa664ca13479338431b774bac1d4be946f02ae55884437d56cf61102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74296339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d24f4eae3bd1ef0502433129b6a64f831fb874fc5f8d501bf808fefd518ce03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 17:06:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 21 May 2025 17:06:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 21 May 2025 17:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 21 May 2025 17:06:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 17:06:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51837d8ad19248820f2edf9b7be692ac6d3f79224261e893794928540cd1093a`  
		Last Modified: Wed, 21 May 2025 18:49:54 GMT  
		Size: 8.1 MB (8062909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc12716d263c1854fba60a93b610acc1777ed00c64e724308ea5b003cb87ac3`  
		Last Modified: Wed, 21 May 2025 18:49:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffdaa08d66d8c01d9a013e7c9475ff55c5869c1825f1e9b1389db8d61f8bdb6`  
		Last Modified: Wed, 21 May 2025 18:49:55 GMT  
		Size: 20.1 MB (20090873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434b626b2e853b9bd0c47469e4a7edc1700a7c5b004ab0fa0e33530c25d3df7f`  
		Last Modified: Wed, 21 May 2025 18:49:55 GMT  
		Size: 21.3 MB (21290151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d09a313cfcb7831bb7d8c542ceb6d27f5939243b1a569f8bd60fd4efda8359f`  
		Last Modified: Wed, 21 May 2025 18:49:56 GMT  
		Size: 21.2 MB (21208008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b81363fb9f71d40d1d06dd23aa9a8b7141cc505e802fe9219ff8721eb3be30`  
		Last Modified: Wed, 21 May 2025 18:49:56 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afa799a23cb992d26939280aca6c24494a91f64be379603c0fecace3f0751fe`  
		Last Modified: Wed, 21 May 2025 18:49:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b51a23ac0aa4b570d00a7300e8bcd3726e1ca421b2e09b95370c0cd88942b`  
		Last Modified: Wed, 21 May 2025 18:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:883f46c58a02dba32bcb183d29e7935470b34cb6eb15d4a5bd0dffd25f565b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8946206e32e81fdc248f0743ed2559ab512a8b26cd1a6c91aa3019d6c9009d57`

```dockerfile
```

-	Layers:
	-	`sha256:bd4e68442ac39155d0de2506127b2f421361d4ac4b2e3ee58554f9519e8b0fb2`  
		Last Modified: Wed, 21 May 2025 18:49:54 GMT  
		Size: 37.9 KB (37911 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f12d8a0d9bc4772ca6ba0634a92d0f086c5cfa23ce0b1c82ed984ae51e55ba99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69326884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ab3ac6528b32639aed4fde55e4d4d9045b4d628e7e646b8460d17485a7e4cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 17:06:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 21 May 2025 17:06:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 21 May 2025 17:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 21 May 2025 17:06:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 17:06:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da9b0b6e5db5763d752fbe340551b18f77636d702b049f2a7caa844165eea6`  
		Last Modified: Mon, 19 May 2025 23:45:43 GMT  
		Size: 18.1 MB (18102612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f70647eb147a91740c8bf7eb26c27af7ebc3464f67b5161b93e458ae0c7b1`  
		Last Modified: Wed, 21 May 2025 21:17:57 GMT  
		Size: 19.9 MB (19943305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a990be4fd91fe635384454a5c47e08ab81e709b51e10b25476690624aff1e72`  
		Last Modified: Wed, 21 May 2025 21:17:57 GMT  
		Size: 19.9 MB (19935934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ce428f605067c622b828a0e2d679e08f91c16f86c4aa638e384aaf2c046bf5`  
		Last Modified: Wed, 21 May 2025 21:17:56 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0838f3c98d2fd644d2f55abad5c127b816d60cba81887a4d5c015b85e94ede5`  
		Last Modified: Wed, 21 May 2025 21:17:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acf5b95d797d91d24860817ecccab76dd2d00e2ec43d31257547cb557a299f`  
		Last Modified: Wed, 21 May 2025 21:17:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bb675210ad153df245f0fa7a22b575269537d8a1200074c511183ffd264b9846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8792edbe75f05b81d88115f3efd7d40c119d42fbeae73ecdcf6c19e1b13b8011`

```dockerfile
```

-	Layers:
	-	`sha256:8d7d60d76dd181bdb0d71a489d428fba7945a69788a2eccf0f826924dc6539f5`  
		Last Modified: Wed, 21 May 2025 21:17:56 GMT  
		Size: 38.1 KB (38064 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4c31e1a5273de0711e580cf1d5e0b45e5ccd208c442f1cfa1b22b8d0966a58fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68343665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bb33826f00a5870ef818c9f16d12f27530bfdae7f03d36e36779e024ee5c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 17:06:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 21 May 2025 17:06:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 21 May 2025 17:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 21 May 2025 17:06:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 17:06:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfb548efcbbbb086aaaaff202f8dcb75387c16103727c68404c07cf6c1e312`  
		Last Modified: Wed, 21 May 2025 21:25:26 GMT  
		Size: 7.3 MB (7301785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41df49181be4cc8df8bb77d160cf22a26623b599261a83cc6d25f4cff68ce237`  
		Last Modified: Wed, 21 May 2025 21:25:26 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c485d3051b351ec38603845abd871f14f9ad19a4a148663c3ed55eaad27d7cad`  
		Last Modified: Wed, 21 May 2025 21:25:27 GMT  
		Size: 18.1 MB (18091486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9b5b40bfe328582a25cf981b1df038e0bd3895b2df68f3cd2ec5477ac741cf`  
		Last Modified: Wed, 21 May 2025 21:25:28 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc42c2a918ccd0bc8d33c6a461e2ee31e177aecd79f3aacd47b9bea954c5b3b4`  
		Last Modified: Wed, 21 May 2025 21:25:28 GMT  
		Size: 19.9 MB (19922888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5595e8b989caddb545869c59098bdf10dda020193432cf29427a1dbf855dd293`  
		Last Modified: Wed, 21 May 2025 21:25:28 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d0a8b02d5bb4dbdadbe7c060943f9da1e1ab230ece33071f3bf6796d7d3bd`  
		Last Modified: Wed, 21 May 2025 21:25:29 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ea01fdc025a5fb28927b7bd80e3e3bf03e1d1f8115507c32170f3c861741ee`  
		Last Modified: Wed, 21 May 2025 21:25:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:435eee87ad1517e4d893488e92ade44ede285e56c3a229f286509cd461167bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8ab780c971ff6873c5682dab884eb5e1cdacaf4018e74d0b1c9bd49d6377d7`

```dockerfile
```

-	Layers:
	-	`sha256:733618f8eada4f4263827f4e0fac766e137b6b1a4182e4125a0c8d7476f3e3df`  
		Last Modified: Wed, 21 May 2025 21:25:26 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:736be430687920dbeb4cb5fc5ae3296eaa1ca6dc83f35a529c134b95e8ea4e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69887190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f753444035a5503f9732c36c59a94474f6a7e1bc66941ddec8aa1c5108673edb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 17:06:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 21 May 2025 17:06:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 17:06:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 21 May 2025 17:06:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 21 May 2025 17:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 21 May 2025 17:06:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 21 May 2025 17:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 17:06:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b618038d9435f5b89cad9da67abac3afab969c8a745d6eb5341959c5fa82ea6`  
		Last Modified: Wed, 21 May 2025 20:06:22 GMT  
		Size: 8.1 MB (8077235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b60745a14fff8d357868c569dedf32326e427c7dfdccad542945eb14a52247`  
		Last Modified: Wed, 21 May 2025 20:06:21 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacfb828377bb616efd5d4ddd35d0bec22d61686dbec2b2a03df699adc7b1e2`  
		Last Modified: Wed, 21 May 2025 20:06:22 GMT  
		Size: 18.9 MB (18910994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76666b2c1651e42759d47b748680ce07a9d2e69f78de7ac55b4b0e42aaf854c`  
		Last Modified: Wed, 21 May 2025 20:06:22 GMT  
		Size: 19.5 MB (19469844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b55412e11f646e93277edd843929b43af20259e80fa8d369a67398207f3237`  
		Last Modified: Wed, 21 May 2025 20:06:23 GMT  
		Size: 19.4 MB (19433940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd0f66b27f31f9db9278fcbd37f755fcd7cc4dcf0ad3835d203b904807d3066`  
		Last Modified: Wed, 21 May 2025 20:06:23 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375446c722fd562400775354a3bed0663e5fc24e03d883e4b426d66082486824`  
		Last Modified: Wed, 21 May 2025 20:06:23 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1939d03f63355453c2971d66e1762ce2718e5d23dbff99d77b793b077d44b1`  
		Last Modified: Wed, 21 May 2025 20:06:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:799e6b17b46fed576600e889ad2514b507aa67dc53e49d2c74d513770f508ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352eaee22ce663bf74b67fba4541c420530b9cd35e7bb08c7b08f17de6dbd69e`

```dockerfile
```

-	Layers:
	-	`sha256:89411131c446b692b675351882c8d96ef7ae967b11af7ca25dd224fc28c0e1db`  
		Last Modified: Wed, 21 May 2025 20:06:21 GMT  
		Size: 38.1 KB (38104 bytes)  
		MIME: application/vnd.in-toto+json
