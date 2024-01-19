## `docker:25-rc-dind`

```console
$ docker pull docker@sha256:8cc36400a2d1ed0bfddcaa53723b43261c5ba84017b50a6f0723652998518ed1
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

### `docker:25-rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:28cc5a19ab2235be0499cb915ecb9622ae0efcc6a51d1e9883a55f0b0cb6691f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122672783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a5b1a7c0c4c481b5a46d52722b933a8fe5c470db8f10d5de1fc9497829d702`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_VERSION=25.0.0-rc.3
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-x86_64'; 			sha256='d350bbbd1c74c0a8542193bd41881afea534b141c6a9d9a27b2f217e51d5c48c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv6'; 			sha256='4a89b48f6a758793d4b40b1ade7bd9e7e2e177e29f05f74abb3fde08f246f0c8'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv7'; 			sha256='2b339b900447394b0cc985d9be30782361828b615ce743c36a9674d4435a2fb9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-aarch64'; 			sha256='9b35494742cc54544cd3f67b162ebfb43435077f02556bfb5a7e1c543f0a2da7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-ppc64le'; 			sha256='68ce36587759f18a9daaf4a11af6db1ba9e4b7089a8062654de38f8b84506647'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-riscv64'; 			sha256='b28cbb99ba1ae9d7b1a4e5d6828a2c2a9b124db2d4f1d226aa71a1f2741aa056'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-s390x'; 			sha256='6177f40328d4004d37b7e422d102d765aeb03e24e202ca8b791a6c000be90665'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jan 2024 22:25:58 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
CMD ["sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
VOLUME [/var/lib/docker]
# Wed, 17 Jan 2024 22:25:58 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 Jan 2024 22:25:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
CMD []
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053db1cba9b36a69c57d12feb977f90ac5cca506592378ee1fc9d5b356fbc771`  
		Last Modified: Thu, 18 Jan 2024 23:03:46 GMT  
		Size: 2.0 MB (2018469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e03b4bcfd30fbc24c85a9b09dcd61cf7f7fb9eba772cf9b939dc833e55321`  
		Last Modified: Thu, 18 Jan 2024 23:03:45 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a310d2c4b9f8c6b5b425fa900c5f7411d9aa6f24934e440607cd573a2064d4`  
		Last Modified: Thu, 18 Jan 2024 23:03:46 GMT  
		Size: 16.9 MB (16894361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bf17531b638252b62e498e010ff1dd695cd292157c6748b9b29393f860074c`  
		Last Modified: Thu, 18 Jan 2024 23:03:46 GMT  
		Size: 17.2 MB (17195294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e847af12a917f457303f254ac8fca57475bfb531348297e7f00009fefadba1d7`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 18.2 MB (18173874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ac817b9e587063873fdc4c0156b1207e2c650471fb76b0e0b00cbdb5a7037a`  
		Last Modified: Thu, 18 Jan 2024 23:03:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcf0b989c2921616630701aae2ba9c622dfadd895e756d462580bc17495ea47`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f70f38f98ff543a6fa31d210a0f5e5f153b7b0fd482197c761c447a72f48af9`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a298fa5e06b931553fefed5c86b886434a818339a3ff4fb0568e3970faf3e111`  
		Last Modified: Thu, 18 Jan 2024 23:58:37 GMT  
		Size: 9.3 MB (9258249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1576ecc98564b8e5998019a0c47011098372860692e9a236dc52c4a5940ab3`  
		Last Modified: Thu, 18 Jan 2024 23:58:37 GMT  
		Size: 83.6 KB (83646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6787a0ebd02f8fa76b69122597a7dcfd8bc6bf6b78a9793727cf579070ff495b`  
		Last Modified: Thu, 18 Jan 2024 23:58:36 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7051ca0403b4e70ba98f47824735e993243b6bdce96b9b73004e87c3a816406f`  
		Last Modified: Thu, 18 Jan 2024 23:58:39 GMT  
		Size: 55.6 MB (55632095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96220f3aaca2efc5f683008a0e35051790b9aa964cbfee5106dcbacc10ee0bd`  
		Last Modified: Thu, 18 Jan 2024 23:58:38 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b9fcfc42cfee34b076685e5727913bc9bbea9e951d18a32f57571a2ba4642e`  
		Last Modified: Thu, 18 Jan 2024 23:58:38 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d93e1ead948d1aa341c7f1fc3eadf63de7263f6906849ec310c525a018c26b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.3 KB (730298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac14a937335c9bf59eea5026fbb9e832945bb2246989a9e34b18daa7e29605ff`

```dockerfile
```

-	Layers:
	-	`sha256:490379f6f16cce2e1e4c27ae3c384a538d04d691ccc684f13a3d3d0d6eed8672`  
		Last Modified: Thu, 18 Jan 2024 23:58:37 GMT  
		Size: 693.8 KB (693791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed4de84ad76a8ea4424756314eade6fc5faa1afeb6ccd97fbfe3e672c29c2745`  
		Last Modified: Thu, 18 Jan 2024 23:58:36 GMT  
		Size: 36.5 KB (36507 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d4af8e0c28516cd5c272af6685429427453e3935812b7987360a16dc18922238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115157816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e114916719200bb06e6ccdf1a4ea6c4fe8b1e0202ea625c853a36227198d25a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_VERSION=25.0.0-rc.3
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-x86_64'; 			sha256='d350bbbd1c74c0a8542193bd41881afea534b141c6a9d9a27b2f217e51d5c48c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv6'; 			sha256='4a89b48f6a758793d4b40b1ade7bd9e7e2e177e29f05f74abb3fde08f246f0c8'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv7'; 			sha256='2b339b900447394b0cc985d9be30782361828b615ce743c36a9674d4435a2fb9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-aarch64'; 			sha256='9b35494742cc54544cd3f67b162ebfb43435077f02556bfb5a7e1c543f0a2da7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-ppc64le'; 			sha256='68ce36587759f18a9daaf4a11af6db1ba9e4b7089a8062654de38f8b84506647'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-riscv64'; 			sha256='b28cbb99ba1ae9d7b1a4e5d6828a2c2a9b124db2d4f1d226aa71a1f2741aa056'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-s390x'; 			sha256='6177f40328d4004d37b7e422d102d765aeb03e24e202ca8b791a6c000be90665'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jan 2024 22:25:58 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
CMD ["sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
VOLUME [/var/lib/docker]
# Wed, 17 Jan 2024 22:25:58 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 Jan 2024 22:25:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
CMD []
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37591cb9dd2cfdfca65b178b489c279ddf98c80db713614ebfb00d8a06b750d1`  
		Last Modified: Thu, 18 Jan 2024 01:07:50 GMT  
		Size: 2.1 MB (2108664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f528fe69dcb5a3cc27e1506619594dc932046c740bf0f8515eb8903ea27eeb2`  
		Last Modified: Thu, 18 Jan 2024 01:07:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f29e7c1e6b71fe0b086d3ff7a5f4a0a77035ed0c69cb591c045718ff0722a1`  
		Last Modified: Thu, 18 Jan 2024 01:07:51 GMT  
		Size: 15.3 MB (15271662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87f71dbd2c565f1b5185d96b8bc8236703dbf2e40704dc77ee81692433e5d3`  
		Last Modified: Thu, 18 Jan 2024 01:07:51 GMT  
		Size: 16.1 MB (16099967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec137b52143802bd0182bbdc6e7179c81ca3bd663ee33f416565b50582d07143`  
		Last Modified: Fri, 19 Jan 2024 00:06:39 GMT  
		Size: 17.2 MB (17172401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68236f4affdea05acdeb4717394d216bf898c12b29c98f61ef83670184fca1b`  
		Last Modified: Fri, 19 Jan 2024 00:06:38 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d298071b11ff7d1f0a923b08236e654ed2ac48dc57a79f8f08e99bc9561de61`  
		Last Modified: Fri, 19 Jan 2024 00:06:38 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d48a806856da2d55ddce34d3a3a4179574485a240b87e29ff866ebc5be62df`  
		Last Modified: Fri, 19 Jan 2024 00:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ebbe8e8a943f5f80fe4b172b095ab23f3c358f8ca4a8402ff44f32433b3edc`  
		Last Modified: Fri, 19 Jan 2024 06:32:28 GMT  
		Size: 9.2 MB (9234252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a4fe4a3eba075c89047d2c57af61434257fcc66776e1375055c5a9341efc52`  
		Last Modified: Fri, 19 Jan 2024 06:32:27 GMT  
		Size: 82.6 KB (82606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07361bb77bb2382a4504254c36745243e4cd4a16062756573185926219e46189`  
		Last Modified: Fri, 19 Jan 2024 06:32:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ff7269e7774918e36c71ad9fcb56cd733699c598634b77f766e0acea4d96d6`  
		Last Modified: Fri, 19 Jan 2024 06:32:29 GMT  
		Size: 52.0 MB (52014793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4401cdd56e6b82726eba1a754a8a828e0df51f734548682cfbe9b9665057eb33`  
		Last Modified: Fri, 19 Jan 2024 06:32:28 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20d9c50fa5dd29eb9bbce15b7bdbc63ea372fd86b0e8ac783add2d8be976043`  
		Last Modified: Fri, 19 Jan 2024 06:32:28 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e6dd5b4a1f2b1b1e70720a845d4abb548cfea83e4266577716d8b6f93a13bde5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427942928c0c568afcc3a1c19a03f3d936eccedb722fa90453b2c39bfcac182d`

```dockerfile
```

-	Layers:
	-	`sha256:0aa9144e152a6ad292521b0a047a759273bcdc29a94e8096614673a6f9c1bc87`  
		Last Modified: Fri, 19 Jan 2024 06:32:27 GMT  
		Size: 36.5 KB (36500 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:6352c185a0b669b0b7cb6ae25ccc95b3260b982d0a1872841da1f9181c41c56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113819467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1647129f9f6e3082ea5540614daf6fbee6b91e67b451f05630533c54cc9373cb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_VERSION=25.0.0-rc.3
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-x86_64'; 			sha256='d350bbbd1c74c0a8542193bd41881afea534b141c6a9d9a27b2f217e51d5c48c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv6'; 			sha256='4a89b48f6a758793d4b40b1ade7bd9e7e2e177e29f05f74abb3fde08f246f0c8'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv7'; 			sha256='2b339b900447394b0cc985d9be30782361828b615ce743c36a9674d4435a2fb9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-aarch64'; 			sha256='9b35494742cc54544cd3f67b162ebfb43435077f02556bfb5a7e1c543f0a2da7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-ppc64le'; 			sha256='68ce36587759f18a9daaf4a11af6db1ba9e4b7089a8062654de38f8b84506647'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-riscv64'; 			sha256='b28cbb99ba1ae9d7b1a4e5d6828a2c2a9b124db2d4f1d226aa71a1f2741aa056'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-s390x'; 			sha256='6177f40328d4004d37b7e422d102d765aeb03e24e202ca8b791a6c000be90665'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jan 2024 22:25:58 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
CMD ["sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
VOLUME [/var/lib/docker]
# Wed, 17 Jan 2024 22:25:58 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 Jan 2024 22:25:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
CMD []
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
	-	`sha256:8905ec7e76e170fa811849878f8b67920dd69d387edf7f89802806eea417feac`  
		Last Modified: Thu, 18 Jan 2024 13:41:23 GMT  
		Size: 15.3 MB (15267802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f32428f6380c92fe7ea56d258c62a37aaa1d8db737be15612814fdf9dc6f294`  
		Last Modified: Thu, 18 Jan 2024 13:41:23 GMT  
		Size: 16.1 MB (16084092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a21c59c2af728af797a8b76eb6d92eebd2377ca91e41ed089ff56e16eb714a6`  
		Last Modified: Fri, 19 Jan 2024 07:09:23 GMT  
		Size: 17.2 MB (17162099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f254a22419fa94b0a4957076951a028c7c11ace37f7005be695759390d56dc71`  
		Last Modified: Fri, 19 Jan 2024 07:09:22 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc15f0663512f42c35970bf63c7fbe204cec46312285f8744477685444547c18`  
		Last Modified: Fri, 19 Jan 2024 07:09:22 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1108ffd60ac566b27ca64268468b1332b65fea986626cd0fda81e1af95554d2a`  
		Last Modified: Fri, 19 Jan 2024 07:09:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548613d16880e3d28526cd0e02cfdb52989c7257b6f18faec7ea5347cc7309c9`  
		Last Modified: Fri, 19 Jan 2024 08:42:26 GMT  
		Size: 8.4 MB (8396070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fddd79a381ec792c311315d4646cc50fd97588ccae48a60d17132f50184383`  
		Last Modified: Fri, 19 Jan 2024 08:42:25 GMT  
		Size: 78.9 KB (78887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96845f855ffcd8cce583534b8a6dc3583e837b528940dcfe7041e733009e6c01`  
		Last Modified: Fri, 19 Jan 2024 08:42:26 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca3fea58916fc471aebfd7c4c577245bb7238f2d9da406a1259592d304e987c`  
		Last Modified: Fri, 19 Jan 2024 08:42:28 GMT  
		Size: 52.0 MB (52014836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413cd3ffb4bcb48861b7b1ea346a561b309fc2b6e15fc21cc02ff6892f4ecd73`  
		Last Modified: Fri, 19 Jan 2024 08:42:26 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1cd8cfbac2f3870e23c41d83d89d7549b77373175c44c49eca473c2e17614f`  
		Last Modified: Fri, 19 Jan 2024 08:42:27 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:415b8eeb0df92409d16f3bbe7f85737d55aac6c1827f99eb06f0cd7ad17d3b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.6 KB (730575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44c550723600e9ae2faf6e09f0b6ec82693d9f35615130a1420c7cb31bcc876`

```dockerfile
```

-	Layers:
	-	`sha256:313bfd3dd9cefb6ccf6fb0e2822fccbe9764aff85cc716fe49bc9fea05d5e36c`  
		Last Modified: Fri, 19 Jan 2024 08:42:25 GMT  
		Size: 693.9 KB (693859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afded5216b823d4fad8b22ad386e8e46a028e66c5e09e58c5a32ffa920c093a`  
		Last Modified: Fri, 19 Jan 2024 08:42:25 GMT  
		Size: 36.7 KB (36716 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ca4dadc391b302960687c1ca9c3c88f8d06d409c92e19322561bdf7053bdfc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114467811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec3051dd3387e191ef4092e5df9221c9ab834eba42b9a8d16eed5b4bddfa364`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_VERSION=25.0.0-rc.3
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-x86_64'; 			sha256='d350bbbd1c74c0a8542193bd41881afea534b141c6a9d9a27b2f217e51d5c48c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv6'; 			sha256='4a89b48f6a758793d4b40b1ade7bd9e7e2e177e29f05f74abb3fde08f246f0c8'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv7'; 			sha256='2b339b900447394b0cc985d9be30782361828b615ce743c36a9674d4435a2fb9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-aarch64'; 			sha256='9b35494742cc54544cd3f67b162ebfb43435077f02556bfb5a7e1c543f0a2da7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-ppc64le'; 			sha256='68ce36587759f18a9daaf4a11af6db1ba9e4b7089a8062654de38f8b84506647'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-riscv64'; 			sha256='b28cbb99ba1ae9d7b1a4e5d6828a2c2a9b124db2d4f1d226aa71a1f2741aa056'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-s390x'; 			sha256='6177f40328d4004d37b7e422d102d765aeb03e24e202ca8b791a6c000be90665'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Jan 2024 22:25:58 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
CMD ["sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
VOLUME [/var/lib/docker]
# Wed, 17 Jan 2024 22:25:58 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 Jan 2024 22:25:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 Jan 2024 22:25:58 GMT
CMD []
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
	-	`sha256:45bda4c4500e6f4efd78f5e9b154f8b64d8824bc0a0dc63130b2f58aefb0eea7`  
		Last Modified: Thu, 18 Jan 2024 09:20:49 GMT  
		Size: 15.9 MB (15901617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e588a2c374a1928abd276a93ed413028bd23121e8caebc1ff13c72a20a6cdede`  
		Last Modified: Thu, 18 Jan 2024 09:20:49 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e0f08772c3bab17eebbae11d31795ea77426f32db32608099958f7aec45c0d`  
		Last Modified: Fri, 19 Jan 2024 02:42:00 GMT  
		Size: 16.6 MB (16610372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e6caeb5ea524285b148bb7a99e173e4d7f0922c66fe4bfc9870cc87990ad5`  
		Last Modified: Fri, 19 Jan 2024 02:42:00 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000e08cbec4cca0d51207559b346d621706f483e596c0cf74e30c666fdcb9d58`  
		Last Modified: Fri, 19 Jan 2024 02:41:59 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b381878972dabfe8b430c63c8ad2e80823ff4b120d36cfdb12f843b782603c2`  
		Last Modified: Fri, 19 Jan 2024 02:42:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174a719f8d0454ab1b9961e0afd628e7c613f6ff4fd93fe708b84eb1fc13c9da`  
		Last Modified: Fri, 19 Jan 2024 03:37:24 GMT  
		Size: 9.5 MB (9509880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19763ef59c2fa8980e32e22ce0fa59baee95117b687adc7cb665226b5441384`  
		Last Modified: Fri, 19 Jan 2024 03:37:24 GMT  
		Size: 93.1 KB (93065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc04a976cf540194caa0913b79aba1fd18a858d67af849bcf71f92c9aea7588`  
		Last Modified: Fri, 19 Jan 2024 03:37:24 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14f8de43dce58de7fb2363c00ce0457fec1f6bfdb083447c2ee142177d64fda`  
		Last Modified: Fri, 19 Jan 2024 03:37:26 GMT  
		Size: 51.3 MB (51341263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccb1f40092d749b55b09320c294575bfba01eafca54ec19ad66c6b66a4719a7`  
		Last Modified: Fri, 19 Jan 2024 03:37:25 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298a0532d23e9603ac76021cb2104914785686b30b75bd371fe41cfa7c9f7698`  
		Last Modified: Fri, 19 Jan 2024 03:37:25 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9703392b45fec61a31e6925c72fa109175e70413d853c1b1d51a2d61a321ff29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.4 KB (730389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31c93890995cdde49f7630d4ae05925824241e64debdee75611e692d4e27331`

```dockerfile
```

-	Layers:
	-	`sha256:fd0e5d05960fe8009814781302688fb2e83141a4eb5b646e554d6fedc9727218`  
		Last Modified: Fri, 19 Jan 2024 03:37:24 GMT  
		Size: 693.8 KB (693810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f94d82fe0cbfbd3a58d6124b1a2a6efe003226a47fb5f1326bb50c4da5bd8db2`  
		Last Modified: Fri, 19 Jan 2024 03:37:23 GMT  
		Size: 36.6 KB (36579 bytes)  
		MIME: application/vnd.in-toto+json
