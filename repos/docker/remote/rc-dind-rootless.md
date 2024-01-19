## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:ebad55fcc43117f761bd368273e686ba7b03237f1bc56f3ce7b6c4c64893e2f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

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

### `docker:rc-dind-rootless` - unknown; unknown

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

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:868cb630655254c267509d84331a4c49fbe93b1835fa3a15fd9bf378288b4343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138317734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2789c497e6695b6f47c27585ca3f83320107859b71f48cb2373edcc3285b5c49`
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
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Wed, 17 Jan 2024 22:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-x86_64'; 			sha256='43fb39c0bc24ac796123935032eddcfb57a7acd9216badeb10714c986ea1e090'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv6'; 			sha256='cb407cfd396892cc0317ef48570492d7e59445a9f50e92181fdf637548801d55'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv7'; 			sha256='936b474e24a51a51fd797bd18290da6abf72d62a614d8730a1fed3deae816ed5'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-aarch64'; 			sha256='d23d03be5880a2f6555932c572ddbc87bd0e1c4c1985933b7488d948eb2494ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-ppc64le'; 			sha256='f52678e23b143b26c2ee20af4ac105ed571bb2e8e39d59478e04bd2d81cbe27c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-riscv64'; 			sha256='555a373414675ae21cafff8280346c94561457f4be254b5576b22f4b5e8f2ab2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-s390x'; 			sha256='37871d879aa0a73f2ac59dab9805bee751d25208bbe72d7d2ab45956f2e1750a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:3cb046858a7136a861811d4c7e08d64a9d97cf0f568882f944f65ebeb86d262c`  
		Last Modified: Thu, 18 Jan 2024 09:20:49 GMT  
		Size: 16.6 MB (16608013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193655093213917c9f86cde817c497bbf69ea9503d46bd2b9e8411513c95d529`  
		Last Modified: Thu, 18 Jan 2024 09:20:48 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b82c349173507151f380e20c657c35623fe6b1a27d1802abe9f071426522e0`  
		Last Modified: Thu, 18 Jan 2024 09:20:49 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed08ae2145408aeff51af2bc03d0fb8e7e7d813b617d1f95091b9e77179f36`  
		Last Modified: Thu, 18 Jan 2024 09:20:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a9ebd225b51f10e3b399e03d500309c6007af89f3686a558c33b32cdd039d7`  
		Last Modified: Thu, 18 Jan 2024 12:21:51 GMT  
		Size: 9.5 MB (9509886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521831825e3df46ed2f712401556b175226c9e657925f55af7755f90d7898bcc`  
		Last Modified: Thu, 18 Jan 2024 12:21:51 GMT  
		Size: 93.1 KB (93081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f254434d946bd878299ed16a8899335ddb1ee702639b2749a278551da104a920`  
		Last Modified: Thu, 18 Jan 2024 12:21:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8e6f2ff2dcbe0f36f7d1fd4c4425fffe13da1cb0d3ad1562005d0ed9bcc89`  
		Last Modified: Thu, 18 Jan 2024 12:21:53 GMT  
		Size: 51.3 MB (51341268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6018ffe0070d3a636ce3cfe74d0f0499aa4d49350d35389b7da9e44d1e2a9437`  
		Last Modified: Thu, 18 Jan 2024 12:21:52 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2a960455405585368e4c4cf652807ab853ff5ea369062516ec8ff6bf8083b8`  
		Last Modified: Thu, 18 Jan 2024 12:21:52 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621cc2d7c1b3f892aeb12786ecef11dc4aef71b77a27f367e5f19ed7800326f2`  
		Last Modified: Thu, 18 Jan 2024 13:19:28 GMT  
		Size: 1.0 MB (1016243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9034b18aa0d0e19c62e1406da571f81e4af228d8695037fa77773f5380032d`  
		Last Modified: Thu, 18 Jan 2024 13:19:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e0e9b73a53e242a275efd8f0d4808c1a4e324c5d64ddf17205b1e1d7efe0f8`  
		Last Modified: Thu, 18 Jan 2024 13:19:28 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c1497719a1028ce27f1b19bcf4d673298ed276a7d70254faa2b3e770f99cae`  
		Last Modified: Thu, 18 Jan 2024 13:19:30 GMT  
		Size: 22.8 MB (22834384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c34cb06f12f7668d75354839b513fe2ee83f9f3d08fb837908098ef265a89c1`  
		Last Modified: Thu, 18 Jan 2024 13:19:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:727ee81a35ca160cdb99f2b336a06e7c25ea89cabfdda285ce75a9fd1cb86440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.1 KB (770070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d56fb3df56745e7422acf67eae00b748d69a0f1824ab450668e20fac5718144`

```dockerfile
```

-	Layers:
	-	`sha256:0aefbb61407e2a485ff8818e89467187f131109411201092f89e0e10ea13df7c`  
		Last Modified: Thu, 18 Jan 2024 13:19:27 GMT  
		Size: 737.0 KB (737008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55992b9bbf9d727c94436d511be0be0b7c879600d2840f8a9d442037ad5aae9b`  
		Last Modified: Thu, 18 Jan 2024 13:19:27 GMT  
		Size: 33.1 KB (33062 bytes)  
		MIME: application/vnd.in-toto+json
