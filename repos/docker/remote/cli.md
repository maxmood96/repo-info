## `docker:cli`

```console
$ docker pull docker@sha256:23cfbeefc3f4aa9d521bb97e07aff63b9c19eb9f9ba9c32bc8239fbc2b77775b
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
$ docker pull docker@sha256:52d88de2357048962588f26d27598908cd1be13d5e0cfa1523793ecb8f32803f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73652948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deb61ad03625c2200c09cad15db296babe3c4062b62bcd8dea55e309e6dacab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-x86_64'; 			sha256='7bdb2ce2916e5dd0354e5d129892bf96fdcdb1a9ab8eed69b9173e131db4c230'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv6'; 			sha256='dc555cf80a1c5849853a71083f4930790e6515d14c31060de77e6d83bbc996c3'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv7'; 			sha256='50aba1c8fe1eb8efefede3dab9e6c2226ba756a5ffa5cf4f4f5baadaee9a7455'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-aarch64'; 			sha256='a91e930a076b91e6c69f11d1dbe3c06729ae765fb9dbb3f97cb808e784647399'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-ppc64le'; 			sha256='fa6b67a69916a99d14191df5dee1e8399d5eb07f1d322f04caa2078045cb0140'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-riscv64'; 			sha256='c582635c0c4fb1e692dd8a7de206373866f2aa3fcfd9cf03d2358585e602e15d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-s390x'; 			sha256='8cb63254106ceded2373a86355f48ea410564e748521a4b097e3d43b93c05e24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 17 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98ba9902857ddbb8552004010cb7e9d38ec727cb6023b99c5c8eb3fd4ce6081`  
		Last Modified: Thu, 17 Apr 2025 18:27:38 GMT  
		Size: 8.1 MB (8062893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c58f351bf97fd28e58cd8060cef8a6f34d9c092e35a3a429552862a9b80da1`  
		Last Modified: Thu, 17 Apr 2025 18:27:37 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fbe10d2a92f2d8205b7fe7a61aa3f5de4275dfff73384f00e215cadef52f23`  
		Last Modified: Thu, 17 Apr 2025 18:27:38 GMT  
		Size: 19.6 MB (19565542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09cf47617ff6abf5514035959688907e7f54de6ac3061a82a07a38d339675a9`  
		Last Modified: Thu, 17 Apr 2025 18:27:38 GMT  
		Size: 21.5 MB (21456647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9167b1a9e2a49008626c0da4079fb7fc4185f701466445fabf46d4fcadf1c4`  
		Last Modified: Thu, 17 Apr 2025 18:27:38 GMT  
		Size: 20.9 MB (20923468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d66e70b322ddce654027aef73f3f8a95a24d341fe1fea3f755072f42e16a70e`  
		Last Modified: Thu, 17 Apr 2025 18:27:39 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6ad03f16d499462ef3e149f7d35f2171dd287cd29105b97831a8da33583e86`  
		Last Modified: Thu, 17 Apr 2025 18:27:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4658f721145adb14dde848bcf6c0620cb4c1b9ef27025ca588e6cc77ddf48e`  
		Last Modified: Thu, 17 Apr 2025 18:27:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:bed48dffce491e86191ef39ace19f81a2e044e5401a8d6e8113c30dd908057d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aea4a8d4ac8b8867270838ac3bd213d1c9d134128501dd403ec934bfe16a36e`

```dockerfile
```

-	Layers:
	-	`sha256:f61c57a32213435eba0c6b56580018ac6cfbe388950fbea0037bcc1f54aec289`  
		Last Modified: Thu, 17 Apr 2025 18:27:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:976b17c9d79aadcf387020b276b1620f5578cd5ad57011b1fe492c700cecdb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68611022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf5eb5389a8724919b6ccd89b41c8136d76061e1ea37a46a737e431f20b44c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-x86_64'; 			sha256='7bdb2ce2916e5dd0354e5d129892bf96fdcdb1a9ab8eed69b9173e131db4c230'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv6'; 			sha256='dc555cf80a1c5849853a71083f4930790e6515d14c31060de77e6d83bbc996c3'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv7'; 			sha256='50aba1c8fe1eb8efefede3dab9e6c2226ba756a5ffa5cf4f4f5baadaee9a7455'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-aarch64'; 			sha256='a91e930a076b91e6c69f11d1dbe3c06729ae765fb9dbb3f97cb808e784647399'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-ppc64le'; 			sha256='fa6b67a69916a99d14191df5dee1e8399d5eb07f1d322f04caa2078045cb0140'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-riscv64'; 			sha256='c582635c0c4fb1e692dd8a7de206373866f2aa3fcfd9cf03d2358585e602e15d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-s390x'; 			sha256='8cb63254106ceded2373a86355f48ea410564e748521a4b097e3d43b93c05e24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 17 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
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
	-	`sha256:8adf473a27e29a258983cb420fbb9e1b8eb738c8df934e10bd9cf65f8e3b3818`  
		Last Modified: Thu, 17 Apr 2025 18:37:41 GMT  
		Size: 17.5 MB (17512375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9a06738d784bf4e963932fa09b019d5070323c9534324cdd5b6534de7d9bdb`  
		Last Modified: Thu, 17 Apr 2025 18:37:41 GMT  
		Size: 20.1 MB (20075420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd128f280e440fd59f8125420e2ee27393cbd8a4f624ecb6150418b8d5e09c6`  
		Last Modified: Thu, 17 Apr 2025 18:37:41 GMT  
		Size: 19.7 MB (19678196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948f18c9fc1eb05aa1ad4c59270c2b97935ef90ce42f7294717700b08b8a6a1a`  
		Last Modified: Thu, 17 Apr 2025 18:37:40 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965e6b27a4811e4b67ff12dd913227fd58ec2b50097afa4fbf034adffdf2391`  
		Last Modified: Thu, 17 Apr 2025 18:37:41 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6359ce0f810633f17052402705d1547ea3c8af51eff1a9a0ca7df3c7c37239`  
		Last Modified: Thu, 17 Apr 2025 18:37:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:03f4c260d41dd0e996485037f1b9ffef9f444f1ca91a61445ba81756e795e8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c20cab2d97bf3bc5fb66556065c08457a53ddb5a5a9968554786cf4a1d00dc`

```dockerfile
```

-	Layers:
	-	`sha256:5d4618616647f7f5308a2b25569464bbbacc5520ceea1774cc737aae46e2edea`  
		Last Modified: Thu, 17 Apr 2025 18:37:40 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f6b490990228b32d94ae1278f88635fc2e1d93142499ceb34c1fbb85c8380589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67614456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c294c0838b5dd0f46960db67103d333f672db373138f1b3bca47fb8a7dafd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-x86_64'; 			sha256='7bdb2ce2916e5dd0354e5d129892bf96fdcdb1a9ab8eed69b9173e131db4c230'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv6'; 			sha256='dc555cf80a1c5849853a71083f4930790e6515d14c31060de77e6d83bbc996c3'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv7'; 			sha256='50aba1c8fe1eb8efefede3dab9e6c2226ba756a5ffa5cf4f4f5baadaee9a7455'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-aarch64'; 			sha256='a91e930a076b91e6c69f11d1dbe3c06729ae765fb9dbb3f97cb808e784647399'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-ppc64le'; 			sha256='fa6b67a69916a99d14191df5dee1e8399d5eb07f1d322f04caa2078045cb0140'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-riscv64'; 			sha256='c582635c0c4fb1e692dd8a7de206373866f2aa3fcfd9cf03d2358585e602e15d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-s390x'; 			sha256='8cb63254106ceded2373a86355f48ea410564e748521a4b097e3d43b93c05e24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 17 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a864060af87a5048c5c602ac87964067948691631141ffc3818333edb16ed6`  
		Last Modified: Tue, 15 Apr 2025 22:13:41 GMT  
		Size: 7.3 MB (7301755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c418fb5b9eb8648b75bfdc32d3b64717b14e09489dfedf7e46fc76341ad53`  
		Last Modified: Tue, 15 Apr 2025 22:13:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c02a9075e72ac575ac987686b524566b5f2b30af5e1b60e0c5547721e21b2a`  
		Last Modified: Thu, 17 Apr 2025 18:47:51 GMT  
		Size: 17.5 MB (17499394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9b808cc99ebc19e3353f54a0387e28e34c83321d3ab3e2d4ecccef5948bbc7`  
		Last Modified: Thu, 17 Apr 2025 18:47:51 GMT  
		Size: 20.1 MB (20055853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb98544edcd3c20cfc258994aed0930a970ca38bcb51299e8ef913cf8c16d4c`  
		Last Modified: Thu, 17 Apr 2025 18:47:51 GMT  
		Size: 19.7 MB (19657168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06763d10183a86dd09b104d5ad2b23d1690346d0c33dacc59a12d108ae524faf`  
		Last Modified: Thu, 17 Apr 2025 18:47:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c62ac809958758f2c08a74c22018ef77d4d7fb57611bba964b0d7be94ae26ae`  
		Last Modified: Thu, 17 Apr 2025 18:47:51 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e9723ac14fe6cee302b4cb5f7690a28a211d0dfb16d4871a92c564e8dbb80d`  
		Last Modified: Thu, 17 Apr 2025 18:47:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0074b191fefcd2671ee2ef868b889e1c37900ec53186fbd05d3859d701b0194f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0179e3cecec651439cd64ff00de3dd60cb8beb8d33868f2a09806ea1db0f8`

```dockerfile
```

-	Layers:
	-	`sha256:e0b21c112521c52dda1e986c3f5a6db7d546098fe5db90c8fbc5cfe35109abff`  
		Last Modified: Thu, 17 Apr 2025 18:47:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68303eb35ec3a17a21c305d5abafa4cf56cfb4e0c55995505fbdb04edfe57c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69433624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b53b676688ea63e108cececef7c952a275896e39c37122f36892a0868391f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-x86_64'; 			sha256='7bdb2ce2916e5dd0354e5d129892bf96fdcdb1a9ab8eed69b9173e131db4c230'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv6'; 			sha256='dc555cf80a1c5849853a71083f4930790e6515d14c31060de77e6d83bbc996c3'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv7'; 			sha256='50aba1c8fe1eb8efefede3dab9e6c2226ba756a5ffa5cf4f4f5baadaee9a7455'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-aarch64'; 			sha256='a91e930a076b91e6c69f11d1dbe3c06729ae765fb9dbb3f97cb808e784647399'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-ppc64le'; 			sha256='fa6b67a69916a99d14191df5dee1e8399d5eb07f1d322f04caa2078045cb0140'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-riscv64'; 			sha256='c582635c0c4fb1e692dd8a7de206373866f2aa3fcfd9cf03d2358585e602e15d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-s390x'; 			sha256='8cb63254106ceded2373a86355f48ea410564e748521a4b097e3d43b93c05e24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 17 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0757cec9b8247b57760f8b7130dddfcd875393c0b6fe5b8594e1436bda11e0`  
		Last Modified: Thu, 17 Apr 2025 18:50:46 GMT  
		Size: 8.1 MB (8077204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdc4631afb83d6365951521e4c046c2514791d363972aa8113ff0005204a4ca`  
		Last Modified: Thu, 17 Apr 2025 18:50:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a78f3d251baf12455053c55dc15e95b86aee510a7100848d03aacd66714760`  
		Last Modified: Thu, 17 Apr 2025 18:50:46 GMT  
		Size: 18.5 MB (18485728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72baf470aa0e1470980f0235fdf31e788c64a43253424be724d7c2e2110aee0d`  
		Last Modified: Thu, 17 Apr 2025 18:50:47 GMT  
		Size: 19.7 MB (19692490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2f9cad1a5086226688db1f3525de29b7fe714033dd8a68897dadd9917eada`  
		Last Modified: Thu, 17 Apr 2025 18:50:47 GMT  
		Size: 19.2 MB (19183018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d2fecf01b5569a6912eb88aef721d7af007ca0f636af39f65bc32fe26368a2`  
		Last Modified: Thu, 17 Apr 2025 18:50:47 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d6874a88f7d04bdcbf76e8214df85bf4c88c14f5b7ff0ad9a9b420db1ae81`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afad8ac09d3c53cc6eef808746d7bc9fc4ed8150e82472e70b689990e157d5fc`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:10193cd16309c1c701e67561f2d98cacaeb1901ed358fd016e613384a52eff8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045be3683929bf108fcbd2bf97b6eadad5bac7f3168464e62009e63aa7568182`

```dockerfile
```

-	Layers:
	-	`sha256:bd4fad60791b68af4c6c575d9a4db26bc6009d708c47251c8bd049b8b827b678`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json
