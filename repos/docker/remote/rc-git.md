## `docker:rc-git`

```console
$ docker pull docker@sha256:0f3b3f271dfaa8d2310632f357a716f62bd59f78005dfdbddb51f922c69c26ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-git` - linux; amd64

```console
$ docker pull docker@sha256:6633b38fb0875ea882c8332173ccc535549c284a1c53a66aeb14bde7f0559154
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45084535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4ffc564e0ab92f682d5a213cad82d932f56965bfa20144672bed82696f1014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 09 Aug 2022 18:20:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:20:49 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Tue, 09 Aug 2022 18:20:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 19 Aug 2022 00:19:27 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 19 Aug 2022 00:19:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 19 Aug 2022 00:19:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.9.0
# Fri, 19 Aug 2022 00:19:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-x86_64'; 			sha256='3be9ce88ecba41b734e3fc8e59a9b11531133761414a78827d1615aadb5ef1f5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-armv6'; 			sha256='2ea0f36350f81ae66db2b8c12104de6ed974a328557a4967857ee6e8df4b8f26'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-armv7'; 			sha256='658db542e40c8063cdafc23f650493bedc10b41b6d6fb581b7866bfeb5ffb0ba'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-aarch64'; 			sha256='6d227b060b2bc3dc5f315a07ae4f647f042755691e2da905b1a21e60a8ae3ddf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-ppc64le'; 			sha256='101ea490283f3c862e9bb4e7ef2a3fb38393cf2139f2b78e7a7423c91ad0c1fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-s390x'; 			sha256='0826c101e1d1a070e8ab8d7649c0da3cb9e6ecf1e717c545188243be6e676d00'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 19 Aug 2022 00:19:31 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 19 Aug 2022 00:19:31 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 19 Aug 2022 00:19:31 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Aug 2022 00:19:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 19 Aug 2022 00:19:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Aug 2022 00:19:32 GMT
CMD ["sh"]
# Fri, 19 Aug 2022 00:19:57 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb510456a427665c9755e7417ad432e68b6e95a1a9a6665f72f0adc6f9ec59d`  
		Last Modified: Tue, 09 Aug 2022 18:22:44 GMT  
		Size: 2.0 MB (2036045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4627ba0696d0614a94c97a4b5c212e055112e2a8f0831f342f3b138955035153`  
		Last Modified: Tue, 09 Aug 2022 18:22:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d957832b8a49136f6d95f00340a0c764c8cd051be7514885f8fca6a80053215`  
		Last Modified: Tue, 09 Aug 2022 18:22:45 GMT  
		Size: 8.7 MB (8706435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd48969715b862016850752e05193de3fe3dbc355a5f277cece7c52d69f4793`  
		Last Modified: Fri, 19 Aug 2022 00:21:18 GMT  
		Size: 15.2 MB (15204103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ff23f60bbeb0724c81569e50d32dfcafcdb6756b2fcc190fce92f5947df373`  
		Last Modified: Fri, 19 Aug 2022 00:21:17 GMT  
		Size: 9.4 MB (9385858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7d8615652c29aa697ce2a5b140de4b1eba2cda84ef7cf2da72243ca1c4b89f`  
		Last Modified: Fri, 19 Aug 2022 00:21:16 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b19992a3fcafdc3e488b63395d06edcf87cb8f375f0976aaf91667138c3794c`  
		Last Modified: Fri, 19 Aug 2022 00:21:15 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e20ee491481b3fac0b1a47f0451031d49e79342978e170a1609901abf32baf`  
		Last Modified: Fri, 19 Aug 2022 00:21:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264d7a61cd0e8337de4b507a4bf992a928439a4f51ff94228b64dac552a0dd6f`  
		Last Modified: Fri, 19 Aug 2022 00:22:30 GMT  
		Size: 6.9 MB (6944169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6ae5f4dc85a4424941397322b7b6e929ff11930d8397a09bf97d981af046de39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42188561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f7059553e2c4265ee7ca6b2c6bb4e9f207182572c8ba429945e50e15da29a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:24:48 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 09 Aug 2022 18:24:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:24:50 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Tue, 09 Aug 2022 18:24:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Wed, 17 Aug 2022 02:16:04 GMT
ENV DOCKER_BUILDX_VERSION=0.9.0
# Wed, 17 Aug 2022 02:16:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.0/buildx-v0.9.0.linux-amd64'; 			sha256='513e2cb7e71a21e20ae7709eb2fcc98d66117bd440d98602a84835e5cd3179bf'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.0/buildx-v0.9.0.linux-arm-v6'; 			sha256='fe7390cc5a72420a5661cd580eedf08808d9271a305bdc32e00841fb2f44c5d9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.0/buildx-v0.9.0.linux-arm-v7'; 			sha256='35d7ee9bb8ddee9715c27ad5fa1512d56dd3b3c6a13137699643d07a932eb08b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.0/buildx-v0.9.0.linux-arm64'; 			sha256='c288ee151a30eb6afe68937600c96eb4b6e1932c9ef46584304438b85756cea6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.0/buildx-v0.9.0.linux-ppc64le'; 			sha256='4a324d4ae294526c9e5f3c6544a9c95009537eb38530e3fbb0940dd3f9b8d6d6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.0/buildx-v0.9.0.linux-riscv64'; 			sha256='794fdce2c09178dae2c7dafae75aa5c0d888e95164f419820b05e0674675b65d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.0/buildx-v0.9.0.linux-s390x'; 			sha256='81d7d84d05a6e24677d22cd812a5ba1cbfb15e44ccba652f4dfa5e3076bb58ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Wed, 17 Aug 2022 02:16:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.9.0
# Wed, 17 Aug 2022 02:16:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-x86_64'; 			sha256='3be9ce88ecba41b734e3fc8e59a9b11531133761414a78827d1615aadb5ef1f5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-armv6'; 			sha256='2ea0f36350f81ae66db2b8c12104de6ed974a328557a4967857ee6e8df4b8f26'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-armv7'; 			sha256='658db542e40c8063cdafc23f650493bedc10b41b6d6fb581b7866bfeb5ffb0ba'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-aarch64'; 			sha256='6d227b060b2bc3dc5f315a07ae4f647f042755691e2da905b1a21e60a8ae3ddf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-ppc64le'; 			sha256='101ea490283f3c862e9bb4e7ef2a3fb38393cf2139f2b78e7a7423c91ad0c1fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.9.0/docker-compose-linux-s390x'; 			sha256='0826c101e1d1a070e8ab8d7649c0da3cb9e6ecf1e717c545188243be6e676d00'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 17 Aug 2022 02:16:16 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 17 Aug 2022 02:16:17 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 17 Aug 2022 02:16:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Aug 2022 02:16:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 17 Aug 2022 02:16:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Aug 2022 02:16:20 GMT
CMD ["sh"]
# Wed, 17 Aug 2022 02:17:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abd6445c68b28c4fea9c5ead64de6d84bfbcf44d2ea150df466f2efe4ca7ac8`  
		Last Modified: Tue, 09 Aug 2022 18:28:29 GMT  
		Size: 2.0 MB (2010519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6c1cdde4920e39b02e2eaa9a348dd527a363263a4901b3efdf13020d24a917`  
		Last Modified: Tue, 09 Aug 2022 18:28:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1503a42e3097b1eaf3bbc5e72622fc4950bd97ec2439372d2daf9fe4324a21b5`  
		Last Modified: Tue, 09 Aug 2022 18:28:30 GMT  
		Size: 8.0 MB (8048680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e110c631490569c8b8328fe02d5530332b51834a444fff8482ea2095df99fc14`  
		Last Modified: Wed, 17 Aug 2022 02:19:44 GMT  
		Size: 13.8 MB (13764305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01e83b70ed3fd83c9a03ebc97780a60f440da4f144be9a98d2aa5ec166d1953`  
		Last Modified: Wed, 17 Aug 2022 02:19:42 GMT  
		Size: 8.6 MB (8598409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8b672a57d6a4c1bdd3c90a1bd3c9e5c67797d93cbaa07b02e0d76e4792ee72`  
		Last Modified: Wed, 17 Aug 2022 02:19:41 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68ad4b438464b3945b912c65876f3fd16b2bcec28cb859c3b8f3a18c5a0e543`  
		Last Modified: Wed, 17 Aug 2022 02:19:41 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f761227ff773efde8be5c1d2539fb43a069b455bda367100908ccb361017a65a`  
		Last Modified: Wed, 17 Aug 2022 02:19:41 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6a3fdd3ca697e71de23c409abaf6574fe54494599a564d34fbd5a7b309b04b`  
		Last Modified: Wed, 17 Aug 2022 02:21:02 GMT  
		Size: 7.1 MB (7057147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
