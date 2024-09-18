## `docker:rc-cli`

```console
$ docker pull docker@sha256:902791f7ddd254b768e4adb3b92fe11d3dbf2482e7d51a0118ec4ae48abb0840
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
$ docker pull docker@sha256:46222414a47dd4f7510bfafc91990a9806e816b33cb0dec5f74ed8a911879719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67535706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49405346f4f3d9e915817365a9ca116bcb01dbc2cc07b5482cd7faec26ef3262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_VERSION=27.3.0-rc.2
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Sep 2024 16:05:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2bdf3e068f4036d4e620358993b9c593f8ff18d4cf94b49a476add064ba512`  
		Last Modified: Wed, 18 Sep 2024 17:55:59 GMT  
		Size: 7.9 MB (7872607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7d21d8593828d167c51c71bf0af81940e920a1e16c0998d7501a115a044bf9`  
		Last Modified: Wed, 18 Sep 2024 17:55:59 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a56a2c1bc126e03aff15d92c21e6fbf4d72c087a0b342e3560796b818219a7e`  
		Last Modified: Wed, 18 Sep 2024 17:55:59 GMT  
		Size: 18.6 MB (18563598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b768b567568f49cd31ed218304e59c4a8a5e490d5ba5977f5926ca7f2cb50b`  
		Last Modified: Wed, 18 Sep 2024 17:55:59 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3c0342b050b1723e6ff5c85ae2c709679e9fd4d1749f2a8547dac3384fbd09`  
		Last Modified: Wed, 18 Sep 2024 17:56:00 GMT  
		Size: 19.0 MB (19035820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cb0511671bdcbd0a282c497fb55a7b5fbee3c6498d9ddc69488c9d0d2f590b`  
		Last Modified: Wed, 18 Sep 2024 17:56:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d26317001f69b9168bfc04c3eaaad18b84ed642ca3a357a31cf5d82f9b79ba9`  
		Last Modified: Wed, 18 Sep 2024 17:56:00 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba6fa7486022ee24496533ed8f7f2472972769153f77d24ca0522e685407b3b`  
		Last Modified: Wed, 18 Sep 2024 17:56:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:944f6fcfcc578d21b2c1db5437d4c58924be58b9a4406674f2df83f5dc49c21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c554c626d6b158c594513d42ea8cdc0538c958fb79fccfdba8fd08afdf31ea`

```dockerfile
```

-	Layers:
	-	`sha256:1c1977978b6b929bdb0d35b2fb9b35770b0dbcbd04d60bc0ced0903539b3305e`  
		Last Modified: Wed, 18 Sep 2024 17:55:59 GMT  
		Size: 37.7 KB (37710 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2f07f6c0bed5f2ba791bbecad598c958217297658a5d499a5ee16a88089520e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62806346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b23a0a053fd2ee708ddba87d83f8e5043fa89dc9439c40cd2cd11798dc6c5d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_VERSION=27.3.0-rc.2
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Sep 2024 16:05:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b88dedd54972fafbd5435f48a405a3c168c853480fa40cb65d2d1f596876b75`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 16.6 MB (16601931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6028135018d2104e9ecb475c9946204e953b1bc17b467cb140d1bfe0f43fed8a`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 17.1 MB (17145042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168c67a2ba23fd3d5060ce9348cefbbda58a5baed699e16c1216f44cc5bf7182`  
		Last Modified: Wed, 18 Sep 2024 17:55:53 GMT  
		Size: 17.9 MB (17882958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e59c71b5becab249d50597069b4dcf46401b9c18327b016cd57bcc941b308d`  
		Last Modified: Wed, 18 Sep 2024 17:55:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49b731d96047e6ce582b403ee5a1e9573aa3f9d1da088d3e2b4a937661e6003`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6945b9ecfa5213d9472fb391ad9c8ad6754c2e5bd933e0e0209e6b17a510f8cb`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:91d7f65f2d82f4483dd81f13ea95b33ac53a0afb3d4cfc777eaeec6391fb819c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38933ef260c80e98f33542b8da98fcefec806d2c220303d1269d03076b1acf2`

```dockerfile
```

-	Layers:
	-	`sha256:e6076ea618a8939dd8ec079d238cf1177312fdfe9836497a90c401bd97c0ab7e`  
		Last Modified: Wed, 18 Sep 2024 17:55:51 GMT  
		Size: 37.9 KB (37858 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a5d4917868c327225433dc876f8e7b13ea341d5dda43cfdeee1845f74e0ea319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61840559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9137abf16be4900aef31874e82a46ec40769130449e51fd5e4a9f1dccc1900a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_VERSION=27.3.0-rc.2
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Sep 2024 16:05:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d640c7d22de228281c4ec66c10dd5ea8a532fc8a323d0815ff65ef384360831a`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 16.6 MB (16593757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a811ef4412033d501baba976778cfa551aea0dff2948846b9c6ae9d7ce6a378`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b872af86ba3f05099f222986995e7f5276e0c22fc744f592deda8eaf0648243f`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 17.9 MB (17870053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf61247285f0a4c44578ded8e1a0f4e678d87df85d001dba8572838709cdb39`  
		Last Modified: Wed, 18 Sep 2024 17:55:51 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb07e28b546250c6bf327294edb4044e62e3648a0dab3c55a0da05fc917b415`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6945b9ecfa5213d9472fb391ad9c8ad6754c2e5bd933e0e0209e6b17a510f8cb`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:90e6f44e9c2b2da370b13f93dbfb9a5d59e6f01cb114a101705b87056eb110c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e881a7d9d2d7732e7dc645cd587b3ae6fa626def9f255d3e49cdb0032ca2ae`

```dockerfile
```

-	Layers:
	-	`sha256:1ee6df583c9904ebc2a04bf563597c12afc9157b0139a656f28100808bdd90f9`  
		Last Modified: Wed, 18 Sep 2024 17:55:51 GMT  
		Size: 37.9 KB (37858 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8601e26b910778bfc74541549fc21b32aeab2c735eb84e8d0c68d46cb58be3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63801092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8aadb567f13120765352bcc096d64ce4feb77a0f55cfb0ecef84d36e16ff2a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_VERSION=27.3.0-rc.2
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Sep 2024 16:05:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf42ea6ec4cf1c9073558af98b258cd542b42ea4f622b96e85dfd03392cac4a`  
		Last Modified: Wed, 18 Sep 2024 17:55:50 GMT  
		Size: 8.0 MB (7981913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de985b4cdcf74979d8d3c832830f8b3bd95894efdb33f21dc2d697139ec1347`  
		Last Modified: Wed, 18 Sep 2024 17:55:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a444f8ca70188a9e8c70217b108bc2e114a9176ec172fa3f95ba87f264963827`  
		Last Modified: Wed, 18 Sep 2024 17:55:50 GMT  
		Size: 17.5 MB (17514765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75756bde0387e6cce8dc7790ebb53ec0032942f2e34c35941b44aba55763759d`  
		Last Modified: Wed, 18 Sep 2024 17:55:50 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e680cec1690d355c5e2e3283b2fb97aac336deaead54847c91273d2e3ab189df`  
		Last Modified: Wed, 18 Sep 2024 17:55:51 GMT  
		Size: 17.4 MB (17413837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e38ad1d2bda98e99c0b9450a439c012924d7ff9d04188001a5414fa9ed3966`  
		Last Modified: Wed, 18 Sep 2024 17:55:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a3d140f45577c41c2a781652eb827e6fe68273148dd3116c789c309c475ccd`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6945b9ecfa5213d9472fb391ad9c8ad6754c2e5bd933e0e0209e6b17a510f8cb`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fd19b63664212c06bc178d6c2b3e6901bdb52cfd470dac785ddd2221dc1d560e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255be50e93dc5154e195fb36c6fea0f3db481c199e6c887bdc499037241eb181`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ae6b6943edc88fc7de19e0fbf47114941f9eebc0ff221c23893ed91faa370`  
		Last Modified: Wed, 18 Sep 2024 17:55:49 GMT  
		Size: 38.0 KB (38010 bytes)  
		MIME: application/vnd.in-toto+json
