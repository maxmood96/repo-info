## `docker:rc-cli`

```console
$ docker pull docker@sha256:94435285696444f22b522e3dc2aa086e8369697e0d854261819767cd5d9ffd6b
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

### `docker:rc-cli` - unknown; unknown

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

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:7af812a0c5ab73ab9600d9f9318a68daedf413e356f5d034a94f5a4aa8f3e909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69459017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84568eb4a7e28e457e33f0a95b4173a25e18644507311ae4f1f0e65f807360ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 23:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 23:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 23:04:25 GMT
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
	-	`sha256:3e446e816d85aa822b94392668f0e03792476c1b9a9a525c3a44012ff1d77d55`  
		Last Modified: Mon, 19 May 2025 23:45:43 GMT  
		Size: 20.1 MB (20075424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9faa7d2dd3f60fb6928d2af0ef01527a91c3475e74306cd25d2f8c6ffcccd024`  
		Last Modified: Mon, 19 May 2025 23:45:43 GMT  
		Size: 19.9 MB (19935951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d8b5de0ab29e4559d5edf3557576af9ddbeab0fd982202a0181bbcdc4c3bd7`  
		Last Modified: Mon, 19 May 2025 23:45:42 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e43c58aa77b760bab9322cc44f1062b2472f0f01d477932f3a20ac62c32f7`  
		Last Modified: Mon, 19 May 2025 23:45:43 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78475bd08156381724492d94b8439ed5bd0bc8bd0c7f9f29810603f718d93ae`  
		Last Modified: Mon, 19 May 2025 23:45:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6a5392a8a752182dc49b4ae2ffaf4849c320ca5f5a47b5326890d86e97087abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e218fb1d3d89a7c44d28cdf40f2f859086762bcdcb3750cc71b8df74a1b4583`

```dockerfile
```

-	Layers:
	-	`sha256:379c2929604c21c231ed134d44800be747841d15dda835aba63e3bb39c1f3f41`  
		Last Modified: Mon, 19 May 2025 23:45:42 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:6e809243e09066c036144e5bdd3e544c70e1124d4b4cc930311e9454e0b4d6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68472324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a1e239b168e1ba83aebeb59366c0b8f30225c1c43b6afaddf6d4a609bc3983`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 23:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 23:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 23:04:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d088acd453a2810f068374be7c873ecdd373aa8cb73c7fa22edf9c6c6572532d`  
		Last Modified: Mon, 19 May 2025 23:46:14 GMT  
		Size: 7.3 MB (7301852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d61a4a1f1b93be982dd3087d4f4a07517959168fd4962c81f01e0f52003e46`  
		Last Modified: Mon, 19 May 2025 23:46:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6461b4732cbc036c2405ace89d93ccb5a54180bfe74cfbea7cca650af046351`  
		Last Modified: Mon, 19 May 2025 23:46:14 GMT  
		Size: 18.1 MB (18091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d665dac75101201f8fbf6c3272c2d97645b323112c2c0e48f4c17fdfc03cb395`  
		Last Modified: Mon, 19 May 2025 23:46:14 GMT  
		Size: 20.1 MB (20055855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c962f0c63f12a5b50aaa580b7a6d661ff6cfc9a9b3eaf8792ae812494b631c95`  
		Last Modified: Mon, 19 May 2025 23:46:15 GMT  
		Size: 19.9 MB (19922888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ec7407dc40db07a17f6342096db90beb6b864a7439d7c395d4327c7c33cfb6`  
		Last Modified: Mon, 19 May 2025 23:46:15 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d197a79e2b4b3f8147225b2e4230597678007cf45117c4667ce5694cefb1de`  
		Last Modified: Mon, 19 May 2025 23:46:16 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27463e47c9a363d4fca5ee76f3fac35cf25f3871c0261aab9df41f56343195c0`  
		Last Modified: Mon, 19 May 2025 23:46:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9d98281beb80a0f2279ed65d5a299ae1b7d80c07be901d6930610f91a00ff343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa413226b7b5d1c798e2f1edf5b360e5492adc05e989c465a7e78f6cc00464`

```dockerfile
```

-	Layers:
	-	`sha256:26d1a30377a14e5df4788bd3afe176d0c861598b00105e92fa053f0a8ca52c41`  
		Last Modified: Mon, 19 May 2025 23:46:13 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b0cab8d4afd9235ab85313b13f5264863a9893d2653b69c1a76c224023a5e90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70109839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604e553f5a2e72a0642867ec71d7a676a648c47f292356f612ec10506d4d2899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 23:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 23:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 23:04:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fffdd893f2edce36ae9ef8552b4908e678780ed400d81510a7672b934b2c9b`  
		Last Modified: Mon, 19 May 2025 23:45:34 GMT  
		Size: 8.1 MB (8077199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d86e9e1048e11c509f223efe8388ce6b460fb5a34e23a02d017ec34b2c5bebd`  
		Last Modified: Mon, 19 May 2025 23:45:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a880d1d44d4371534ca4b28c80eec1fd2004e1abbfc670ae3454922cfb9ce6`  
		Last Modified: Mon, 19 May 2025 23:45:35 GMT  
		Size: 18.9 MB (18911008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270be18cc17ab6d5b737ac3d5414e12f1f36d49025b5e6e7e87b8b1c0d261551`  
		Last Modified: Mon, 19 May 2025 23:45:35 GMT  
		Size: 19.7 MB (19692500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124b553cb1d277688778d90650228589fbae1a123ea4159b3e86be45dbd881c`  
		Last Modified: Mon, 19 May 2025 23:45:36 GMT  
		Size: 19.4 MB (19433951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913832b1a4edd4b816f250c3430cfd8ebc5fdcc341328eda47ff78a9c6750d2`  
		Last Modified: Mon, 19 May 2025 23:45:36 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53491eeeb37a9988871b3fa80e54941282c1c3b29ca31a668b15ec926957a444`  
		Last Modified: Mon, 19 May 2025 23:45:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529aaaf3143411c3f67529a626ce1cbe3874db6ca52e1a9bb2edfdffb8f03fe1`  
		Last Modified: Mon, 19 May 2025 23:45:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e4dde3d5444bdd19907eb1c74f4fe6318d722c61825acf9b16b42443a21c5725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e2d39505d0bf4ac1e93c732631f30ff9c5d24e2f58725452b829f57ca5f63b`

```dockerfile
```

-	Layers:
	-	`sha256:24bcb8ad2588ce9b10a258305f1f2a74cfca720626de9254f17e203cb52e4bb8`  
		Last Modified: Mon, 19 May 2025 23:45:34 GMT  
		Size: 38.1 KB (38105 bytes)  
		MIME: application/vnd.in-toto+json
