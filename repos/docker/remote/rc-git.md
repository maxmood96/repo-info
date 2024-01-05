## `docker:rc-git`

```console
$ docker pull docker@sha256:0514d5fe6822cdb524eefeaf7947f0dfa88272de46f9e6389f417870bdfa5b1b
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

### `docker:rc-git` - linux; amd64

```console
$ docker pull docker@sha256:cedde3df965c1ab929c51cc02ecae3761e8adbe001f04a1fa28c0eab83b0c15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125225409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1030a37911ad88174b9472b45c2648ad131c9ce87aeff1afefabadd981f9e688`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 13 Nov 2023 22:06:12 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Mon, 13 Nov 2023 22:06:12 GMT
CMD ["/bin/sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Nov 2023 22:06:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
CMD ["sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Nov 2023 22:06:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Nov 2023 22:06:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
CMD []
# Mon, 13 Nov 2023 22:06:12 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba5000a1254dde420992b6af6db58fdcd4862b79adf1d88b81f132f62c7d167`  
		Last Modified: Fri, 05 Jan 2024 01:53:50 GMT  
		Size: 2.0 MB (2018464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f156c17dfe5733ec773b0a8cfd1dc6d7f6096db92373c153b0885fb9f6fa63cf`  
		Last Modified: Fri, 05 Jan 2024 01:53:50 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8945a0bd73b35a234725490a60072a84c657d98a6faa0549ae178d7ac665cc`  
		Last Modified: Fri, 05 Jan 2024 01:53:50 GMT  
		Size: 16.9 MB (16891688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24fb2d4fdcd30abeef62a854a41648a9740e61edba2418218c9097844711484`  
		Last Modified: Fri, 05 Jan 2024 01:53:51 GMT  
		Size: 17.2 MB (17195294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264e7eee16a1639ef22c918c9270fdbfc623240bdad2e3db56a7bc845b413be`  
		Last Modified: Fri, 05 Jan 2024 01:53:51 GMT  
		Size: 17.9 MB (17852072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b887d8e287a3955a7a4f8e63c7c77f668e51ea73929ff8a4954f866cc83c051`  
		Last Modified: Fri, 05 Jan 2024 01:53:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62527c10bf6536c092afc9edbec3656e62baf32146c682d0cc99b07e8df4b69e`  
		Last Modified: Fri, 05 Jan 2024 01:53:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74711a39693f3d9ea89259cabf9ad7a1db2fccd2498531e93c516ad01a59a4dd`  
		Last Modified: Fri, 05 Jan 2024 01:53:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6619ea13ee9b85bb69295b2f00abc9c3041744d84fb1a975ba529e265c77b71a`  
		Last Modified: Fri, 05 Jan 2024 05:47:55 GMT  
		Size: 7.1 MB (7068082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03711b79e228ab0a994b821ff683ecba6d08ac4f416bc8bbdbd8d53c45015cc9`  
		Last Modified: Fri, 05 Jan 2024 05:47:54 GMT  
		Size: 83.6 KB (83644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0fb7c5c631ce11c1f8ac122bf6c21988b2b8fa51b2725aad5dc83522a6f33c`  
		Last Modified: Fri, 05 Jan 2024 05:47:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4eaf8a6b23aa41d376d870478ed953e416fecbcd6ed8c4d78f5ab25d6f1df`  
		Last Modified: Fri, 05 Jan 2024 05:47:57 GMT  
		Size: 55.6 MB (55578203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85da9a7f6d63f87b67f9f8d26709db974d91b0159aa247cc1e024cebc4fb47b7`  
		Last Modified: Fri, 05 Jan 2024 05:47:55 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658182b0eab05036df69c43db069c862a87b7cbf39b5735812b163c13b396c29`  
		Last Modified: Fri, 05 Jan 2024 05:47:55 GMT  
		Size: 2.9 KB (2874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc81e08ed4b5bcc4b80ec2e75931e459d5c02fb754a04a2a67cce2e8efb00bc`  
		Last Modified: Fri, 05 Jan 2024 07:47:33 GMT  
		Size: 5.1 MB (5121540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-git` - unknown; unknown

```console
$ docker pull docker@sha256:f1e39814f2bfd59818775b851724d2d6b64907a199a4b354164c110ab9932da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.8 KB (744798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a973eddb322ac22e1e42682b10fc303ee28797d31d4499206a9e69872dde20`

```dockerfile
```

-	Layers:
	-	`sha256:b0596e2ca0dc7a220e9e9601d0e039f2db37d7346e136ed590f6212712172f34`  
		Last Modified: Fri, 05 Jan 2024 07:47:33 GMT  
		Size: 731.2 KB (731212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2735db3b0b5743562c9463b87e656212399cb925ea1e2d2a1e6c80f8b7b6aee6`  
		Last Modified: Fri, 05 Jan 2024 07:47:33 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:14646b11336cba65d6f6e176426534f940c572f4fe8280a7871f8887c12015c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117976909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c9e3dabba8deaf17532dc82ac2e0f19032b1be26840b3b5b191c63b993e1ea`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 13 Nov 2023 22:06:12 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Mon, 13 Nov 2023 22:06:12 GMT
CMD ["/bin/sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_VERSION=25.0.0-beta.3
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Nov 2023 22:06:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
CMD ["sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Nov 2023 22:06:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Nov 2023 22:06:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
CMD []
# Mon, 13 Nov 2023 22:06:12 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bbd6f11a587753f7964ed8d3da44e1fea9babbfca054963d48c1d86c91832c`  
		Last Modified: Thu, 21 Dec 2023 22:01:44 GMT  
		Size: 2.1 MB (2108651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e90aa0693158959fa7290f851cf6c0c6f8f6c5f8c79658c8da3534d49fc9f60`  
		Last Modified: Thu, 21 Dec 2023 22:01:45 GMT  
		Size: 15.3 MB (15269026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a67ea298a45ff1985578bb1bb723bbbcadaf80be89899c174b679973dd1bfe`  
		Last Modified: Thu, 21 Dec 2023 22:01:45 GMT  
		Size: 16.1 MB (16099974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b6e310d02060323156fa7d0de83066a238fad80589031e2222944818c28d18`  
		Last Modified: Thu, 21 Dec 2023 22:01:45 GMT  
		Size: 16.9 MB (16867513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15065c9e2f5b64c9043d8ddb30c73e6e235a6610e5dbc3ad84ab68daa34d0bb1`  
		Last Modified: Thu, 21 Dec 2023 22:01:45 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e135adec007507c4b2d1cbf19eeecc65f612e0b2376d71c42d04a21a1b23186f`  
		Last Modified: Thu, 21 Dec 2023 22:01:47 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e42b0d05d826f2dc028f35fbe0349d6c1a72d1d7dac8950c95973462c5941a9`  
		Last Modified: Thu, 21 Dec 2023 22:01:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e7346de647b900676a6dfce139f3f4ef4406aafd616f7e6cd6e78d7d8d134`  
		Last Modified: Thu, 21 Dec 2023 23:01:33 GMT  
		Size: 7.4 MB (7362047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4cea29f0213f0bdd40d9de09c88a59efed6e535578bdd11de305e6e120cb11`  
		Last Modified: Thu, 21 Dec 2023 23:01:33 GMT  
		Size: 82.6 KB (82607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53191707f053016637b13e038d378e303ae097591f9202c249ee9cef1a73aa3`  
		Last Modified: Thu, 21 Dec 2023 23:01:33 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c685f7301a8dcaa9273ad0c3acd9ac4fbcdd36011dec16d408fd790c1d163a`  
		Last Modified: Thu, 21 Dec 2023 23:01:35 GMT  
		Size: 51.9 MB (51912903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15542e260bf8065db319ccaabf450e9ab0f0390cc14ac535fea564b402afe3d`  
		Last Modified: Thu, 21 Dec 2023 23:01:34 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d473ebb99de0670c90fe7ec5607913ae4ab35d5582859bceaa574e4f82427707`  
		Last Modified: Thu, 21 Dec 2023 23:01:34 GMT  
		Size: 2.9 KB (2871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e20d27f21855c241d0fe470993a09161400075acf9175e1a4d201bd158cad4`  
		Last Modified: Thu, 21 Dec 2023 23:54:20 GMT  
		Size: 5.1 MB (5101659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-git` - unknown; unknown

```console
$ docker pull docker@sha256:d8de463270c395a2afac33d016c7b46ec6b75f37e4ec452d94e8b0e5e424647c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 KB (13002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f44a32e85c8dcb17e2f90f1b9551f852a71fb7c18f30fd7e1d2af503f572546`

```dockerfile
```

-	Layers:
	-	`sha256:06efe9f65c6086382688d06316a9392aa0503a4feaa388747a70f8d903be0d0d`  
		Last Modified: Thu, 21 Dec 2023 23:54:19 GMT  
		Size: 13.0 KB (13002 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:1f07044acf6dde459d41ea4e6f9cb1f24a8be69fc104da000acdc25189ae1eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116344991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0305a5f6bce98de5eaa1362fcf617405564bbbed4540a3326c3299b0aea059`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 13 Nov 2023 22:06:12 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Mon, 13 Nov 2023 22:06:12 GMT
CMD ["/bin/sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Nov 2023 22:06:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
CMD ["sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Nov 2023 22:06:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Nov 2023 22:06:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
CMD []
# Mon, 13 Nov 2023 22:06:12 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7102b17e4ec828559672f3388bba1ec86d87e7aa09caba4b82fc6870b4fa6`  
		Last Modified: Thu, 14 Dec 2023 22:03:12 GMT  
		Size: 1.9 MB (1888652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f19fa8a6c45d74eb65c7d5844869fef846c8305dd15e21604b2c06e20d1279`  
		Last Modified: Fri, 05 Jan 2024 02:27:22 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1399c95d35da7a273502e48feb8e4fec31ab4fc53455657a7750ec6cb12dc7e`  
		Last Modified: Fri, 05 Jan 2024 02:27:23 GMT  
		Size: 15.3 MB (15265152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da9ff40d4366efb6a51826d6f9444748455e6aeaa7208d93fd17603cc5743ee`  
		Last Modified: Fri, 05 Jan 2024 02:27:23 GMT  
		Size: 16.1 MB (16084084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4197dabf6c1df3d0041e8ac9461e3ebc3309ae1f74cbcec14e228a73e767ee`  
		Last Modified: Fri, 05 Jan 2024 02:27:23 GMT  
		Size: 16.9 MB (16852960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07af02685d6e253b0f361dbf996995f3f0d4d02ee1d13e5ec61880b1e65f50df`  
		Last Modified: Fri, 05 Jan 2024 02:27:23 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837e93f9f247b771545427cc7216dbc2eb479966807f9728567172f1c206883a`  
		Last Modified: Fri, 05 Jan 2024 02:27:24 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41e66a9a8453c4655e6cde0761e0f7662efe2d8b45055e62bf4f720c041863e`  
		Last Modified: Fri, 05 Jan 2024 02:27:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f292e62f92abe017abd9424fdf78a625c9757fd0332367e00b04725d50eea1`  
		Last Modified: Fri, 05 Jan 2024 06:50:39 GMT  
		Size: 6.6 MB (6649830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dbfe8f35077484abd7bb0639c266a98840574cde24708ee844ec49b161e1e4`  
		Last Modified: Fri, 05 Jan 2024 06:50:39 GMT  
		Size: 78.9 KB (78882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ac866111599ca459d36fc6da740964dccc1974888d18c2b433276820340cbe`  
		Last Modified: Fri, 05 Jan 2024 06:50:39 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b56626d4c30440d9eb2c888cd32669e3194af0a99bd9e47445508de0bb0db9`  
		Last Modified: Fri, 05 Jan 2024 06:50:41 GMT  
		Size: 51.9 MB (51941317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8c207384c642d6fc1f3536ef52866ff5390a2e91e1f235086b1d92ce28464c`  
		Last Modified: Fri, 05 Jan 2024 06:50:40 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ced26362ff7f89711aabb953ca0d58b22e340e3751b0b755daac73f0c1622a`  
		Last Modified: Fri, 05 Jan 2024 06:50:40 GMT  
		Size: 2.9 KB (2873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a815122194d56ae063d2759bada29a4b7ff878b582f155c03b130f35b8553d6`  
		Last Modified: Fri, 05 Jan 2024 08:22:34 GMT  
		Size: 4.7 MB (4657474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-git` - unknown; unknown

```console
$ docker pull docker@sha256:374c3b45dc154c4789a2143384310bf9fd86f4e1a504aff380af128162f580c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.4 KB (747385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450a71e3da8ec87316ddd037b3029ac29dd8d84b92418c55387a2d951fa22c9d`

```dockerfile
```

-	Layers:
	-	`sha256:e93be0f0d1649a0c5ea38eb1478f56e1564ddabddee867b4b640b2ce1bc24af9`  
		Last Modified: Fri, 05 Jan 2024 08:22:33 GMT  
		Size: 733.7 KB (733712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c802cb65889fcefc344238a4e662a07b76c3b4d80889d66a08db67cf771a69`  
		Last Modified: Fri, 05 Jan 2024 08:22:32 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bfc333d399ba0eff9ded3259d5e890536893a928ccf859e979c8e8d8b3c0142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117239072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91c0346e8ccb58ec8f5c367bd5b3bf55854782f527342f8bfe64018a38c696d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 13 Nov 2023 22:06:12 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Mon, 13 Nov 2023 22:06:12 GMT
CMD ["/bin/sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Nov 2023 22:06:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
CMD ["sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Nov 2023 22:06:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 22:06:12 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Nov 2023 22:06:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Nov 2023 22:06:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Nov 2023 22:06:12 GMT
CMD []
# Mon, 13 Nov 2023 22:06:12 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4959de38143abac793d31e4e8592696721305ff06281f8b9284aee380afcfe`  
		Last Modified: Thu, 14 Dec 2023 22:04:39 GMT  
		Size: 2.0 MB (2014899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf613c8d3eefad31faacee38beeedf68069e48ea01d8f083fa0a57ce343ed827`  
		Last Modified: Fri, 05 Jan 2024 02:15:00 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f7f5dfc78da18304eb4182d0d9812b54f9f67b404f702bb30a18a258d2e828`  
		Last Modified: Fri, 05 Jan 2024 02:15:01 GMT  
		Size: 15.9 MB (15898968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2016098b7e4307df37c03cade0cbf5bb28dd430b00a643063b47d3b6db5ad797`  
		Last Modified: Fri, 05 Jan 2024 02:15:01 GMT  
		Size: 15.6 MB (15640602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cecda7589ff1bc7873d2dc1c56d43b445f770594fc4ea3b7b9d1685214a58a`  
		Last Modified: Fri, 05 Jan 2024 02:15:01 GMT  
		Size: 16.3 MB (16302321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c192c6cc697f33fbeecd318661d3eee7e68f97c3388f0f3600938a68e79dcffe`  
		Last Modified: Fri, 05 Jan 2024 02:15:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86ce5d0c34db276c50e408daefacb3a1ac83e1c6637f9700733ecccd5991a73`  
		Last Modified: Fri, 05 Jan 2024 02:15:02 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b2e953f6ebfa7fa9a3670bada3a313c7bf0c980bfda49ec6833a8ce5ed04b8`  
		Last Modified: Fri, 05 Jan 2024 02:15:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6f7f4786f805712775b6aa1f98a3bac4626b6e244e917b290a1d6c6ab11ab0`  
		Last Modified: Fri, 05 Jan 2024 06:14:38 GMT  
		Size: 7.4 MB (7428476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d3c9af1066d789d7a2e05047e1361c902e3e775ffd2032b9773ff3002d3331`  
		Last Modified: Fri, 05 Jan 2024 06:14:38 GMT  
		Size: 93.1 KB (93065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f70fc3677175d4db06176178ac5e404fa737e2e8069c46652d0086981d226c`  
		Last Modified: Fri, 05 Jan 2024 06:14:38 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacddf5261725ffbb32419f35641934b5cb58554d1d00654bb6bc32fd3516512`  
		Last Modified: Fri, 05 Jan 2024 06:14:40 GMT  
		Size: 51.3 MB (51277484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d33235a00378c1b792a81b837dc1987ebe3fff28b20071a71d9e814634a399`  
		Last Modified: Fri, 05 Jan 2024 06:14:39 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164512e13b197a35025576209798d17725fa0e2083ab5cc334daf6da37fc998a`  
		Last Modified: Fri, 05 Jan 2024 06:14:39 GMT  
		Size: 2.9 KB (2872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1009f677d5b0b23e5b76ba249454a4c7fc1c1c59d84cc0edf7c559c1705f6037`  
		Last Modified: Fri, 05 Jan 2024 08:14:05 GMT  
		Size: 5.2 MB (5227524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-git` - unknown; unknown

```console
$ docker pull docker@sha256:944d8e9e0c726a0591d905e95df35e287ff7103ebea8ec246debc48e7cf341d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.3 KB (742331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ccc64dd329b8de26d7689533d13faaa82f5370bd05cde1be0bdf2c7c7c0d9b`

```dockerfile
```

-	Layers:
	-	`sha256:1c195e1a89d84c0fb175f3b6e031f56ba7e11522fd3de9b0d52c787159713f8b`  
		Last Modified: Fri, 05 Jan 2024 08:14:04 GMT  
		Size: 731.2 KB (731221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be4452cbe6a9b884ce234e5577452c76bca085164cdfab586740745638f77cc`  
		Last Modified: Fri, 05 Jan 2024 08:14:04 GMT  
		Size: 11.1 KB (11110 bytes)  
		MIME: application/vnd.in-toto+json
