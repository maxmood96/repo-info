## `docker:25-rc-dind-rootless`

```console
$ docker pull docker@sha256:ba698ebdb3898ab17b441b29d8026ec310835ecb72ae7246c08917465392f440
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:25-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:157751e0e97266123fb9570b90da96f134682f4d366d0742c94981544cefb42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144626951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d7242fc31a6e39ab08fdbdaaf39cf05736db875f8741f224707ff3ab89fcd2`
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
# Wed, 17 Jan 2024 22:25:58 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 17 Jan 2024 22:25:58 GMT
USER rootless
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
	-	`sha256:513959e829c86109ccff7445ecef67c87fc11fcefe422f6008317ce3d160f810`  
		Last Modified: Fri, 19 Jan 2024 00:50:49 GMT  
		Size: 974.0 KB (974044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af883f91a29725dd94945849eb36420c0cbd079f294ed22713288b5b80710ec`  
		Last Modified: Fri, 19 Jan 2024 00:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5e4ed7a39e73fa88965ba2ef740a4a4eeba0a75d0639f21217dd24e240852`  
		Last Modified: Fri, 19 Jan 2024 00:50:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c264514174e51642529058ea88a4b482ca0b623815890cdfe85aba4738b6a041`  
		Last Modified: Fri, 19 Jan 2024 00:50:49 GMT  
		Size: 21.0 MB (20978490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fa5fc112221756272a6b68d474d6e030adec062078c5688911aaa71ba44d0d`  
		Last Modified: Fri, 19 Jan 2024 00:50:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6fc23d6a861b634e6e5304ea85681412470c65904bae5c76456d368d0efbf0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.6 KB (769610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0af80036613e76ca685e5119d7a0ab6efb5d707d3f0f5ee7145fca3671e07d`

```dockerfile
```

-	Layers:
	-	`sha256:f9c3618428085ab3154382dd8a459d528cc0834128fedf1d60616081661acda8`  
		Last Modified: Fri, 19 Jan 2024 00:50:49 GMT  
		Size: 736.6 KB (736609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1fd8682a35992351e16894971228f017a77e03d4c2f30667bd8a50c709b260`  
		Last Modified: Fri, 19 Jan 2024 00:50:49 GMT  
		Size: 33.0 KB (33001 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:32b4adc17e5e8b73d592fc5e721e97c050012b6dcf3d55b29c3f766bf519b0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138320008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1f6e65d465d963a0381b87593bd0b56b6fb5bff4ff0b9c5831560ed998ca74`
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
# Wed, 17 Jan 2024 22:25:58 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 17 Jan 2024 22:25:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 17 Jan 2024 22:25:58 GMT
USER rootless
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
	-	`sha256:35a202a41edaf83ddef9c73a2d012203cb6656d52923e27569408402f02cbd52`  
		Last Modified: Fri, 19 Jan 2024 04:39:30 GMT  
		Size: 1.0 MB (1016234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47eb79d7229e30e995df549409bb6b71d66a5a438bf51aab7f49a1c6878de06`  
		Last Modified: Fri, 19 Jan 2024 04:39:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9a9cd38688c82d579ebb254f668745f040adfb588a4f5c337442d2cf123350`  
		Last Modified: Fri, 19 Jan 2024 04:39:29 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f518f45b86bfa58b89d25204c4a276f8d6aca56151f94267494af25239c4872e`  
		Last Modified: Fri, 19 Jan 2024 04:39:30 GMT  
		Size: 22.8 MB (22834327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1e67eb523ab97ff0bde8f5e500426b4105b41d51208f6f384398bacb8f8183`  
		Last Modified: Fri, 19 Jan 2024 04:39:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:df28bd1aefdb19d5d6b25ef76271f7c08f7220ef63f7d9c343d521d9aa05c137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.7 KB (769680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0114e00b3e802b48c4186f734a6d014258b3410287a0dcf63117495975c99`

```dockerfile
```

-	Layers:
	-	`sha256:6654b2bb984654fb357d85b3fe66648184563ddc4fabf0897b6915b7f56e5130`  
		Last Modified: Fri, 19 Jan 2024 04:39:28 GMT  
		Size: 736.6 KB (736618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53e59861f392bbca64d2c52def07e63746f8541103a4af0ed89dcb87eda28186`  
		Last Modified: Fri, 19 Jan 2024 04:39:28 GMT  
		Size: 33.1 KB (33062 bytes)  
		MIME: application/vnd.in-toto+json
