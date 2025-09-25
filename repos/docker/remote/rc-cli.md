## `docker:rc-cli`

```console
$ docker pull docker@sha256:dda1e234e0cb23ca75a81dac8839aaa3dc45758e5fa99b1d9093c4b9bc9a527a
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
$ docker pull docker@sha256:2934f2c12af881d7f7f4c389a4215ae3c7d2f13d303a0f49049a9f3eff769288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75999417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284c363515906c85be4f96a921c6a8409acfd037d0bb042ccc07dc0a6a9afab1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.4.0-rc.2
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-amd64'; 			sha256='4f5e5a1b6dd0d6ff8476c8def7602d1eeedcb6f602e8dcd45079d352247eba06'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v6'; 			sha256='216ef84b075c270ab2f0bbcf9fcedfb0175226349714a129b7806b4b3f1a460c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v7'; 			sha256='b7184384910ed1b3726f7dc340e3c644640fc5f7028c6ccdfda843cfbcb3fb67'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm64'; 			sha256='e3519d085710d2502c673380f763596ae0b378d0ae8976ccbb14adaed82327ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-ppc64le'; 			sha256='e2bc5c418f680fa7ddb8782eea00a56725189ef672019db62b9f526d120afb08'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-riscv64'; 			sha256='e4f3b40472e3784bf5254eb399aa640205f349ee7c4839db989313d91258b7c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-s390x'; 			sha256='75c24bc03e809ead2e80840280359e3327965c6c1535d0fdc8d48cc86355eecb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Sep 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833ccca71281d2f670d624c393d6a068175fa7904d8dd3dd5426adce828d9c85`  
		Last Modified: Tue, 02 Sep 2025 18:03:49 GMT  
		Size: 8.2 MB (8198133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ecbf662f64e9123b3e218f3f0f6425c734aeeed6202892b35fc55b2886a97a`  
		Last Modified: Tue, 02 Sep 2025 18:03:48 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd52a0ba42c39f576ef7fff41ea9b6924fae9deeaaffbb1c9f1dafc31c7d07d9`  
		Last Modified: Tue, 02 Sep 2025 18:03:50 GMT  
		Size: 20.4 MB (20429620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5228b776ff17a1f9eab1c9a28de5c501b94ac86e449124258d44f45024250068`  
		Last Modified: Tue, 02 Sep 2025 18:04:02 GMT  
		Size: 22.1 MB (22110960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3015d1987319b6bce5524333ff12d8c2bf9023b09c4ffbfe96e8f9a55cdf4b`  
		Last Modified: Tue, 02 Sep 2025 18:03:50 GMT  
		Size: 21.5 MB (21458862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387746d35d3b68a0355d9d040b9c8d6515806a739019e2540c3ff8aaf6ec6f9d`  
		Last Modified: Tue, 02 Sep 2025 18:03:49 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c306c9f14f9de4da5b24c0bbb30aeb319097838405ccba14167b26f6cd6655d1`  
		Last Modified: Tue, 02 Sep 2025 18:03:49 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bec741580771823e7fa20d2a9f8a858202e6c04e5daaf22c430e6c1e8f3d0ef`  
		Last Modified: Tue, 02 Sep 2025 18:03:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9c4ca58ccd0ca1befbde60523ed94a73d47f419fb97047fcd1d468dff18247da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd9c1b7d119b5f4a64b5a41986d423287abe5fdc5608238ff1ab1de9c52b817`

```dockerfile
```

-	Layers:
	-	`sha256:58f1cca4c0369446ea714020cc8569375206376ab5079bef0ac2b43948605c81`  
		Last Modified: Tue, 02 Sep 2025 20:07:49 GMT  
		Size: 37.9 KB (37911 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f699f94023b6974c04faccad386267d1a0b203bc1d9379403140b9ad9e793490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70918040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeae97e20e76f2a6ce27a595fd131e96f2b641392e06dc57bcb907b7a815a277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.4.0-rc.2
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-amd64'; 			sha256='4f5e5a1b6dd0d6ff8476c8def7602d1eeedcb6f602e8dcd45079d352247eba06'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v6'; 			sha256='216ef84b075c270ab2f0bbcf9fcedfb0175226349714a129b7806b4b3f1a460c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v7'; 			sha256='b7184384910ed1b3726f7dc340e3c644640fc5f7028c6ccdfda843cfbcb3fb67'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm64'; 			sha256='e3519d085710d2502c673380f763596ae0b378d0ae8976ccbb14adaed82327ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-ppc64le'; 			sha256='e2bc5c418f680fa7ddb8782eea00a56725189ef672019db62b9f526d120afb08'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-riscv64'; 			sha256='e4f3b40472e3784bf5254eb399aa640205f349ee7c4839db989313d91258b7c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-s390x'; 			sha256='75c24bc03e809ead2e80840280359e3327965c6c1535d0fdc8d48cc86355eecb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Sep 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a7319dae875f7a0eedb0d8dcfc4c97a5928f828700948e8a136178932826cd`  
		Last Modified: Tue, 02 Sep 2025 18:03:06 GMT  
		Size: 18.4 MB (18421940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f063d8a4fda9a260d83c0206516c1534e56046f4377aa06e2e9e817087af74`  
		Last Modified: Tue, 02 Sep 2025 18:03:06 GMT  
		Size: 20.7 MB (20705304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b68edd02334e79e40ca9784cafac0ae7671c041d5e66126c8eb9f82d48a3ab`  
		Last Modified: Tue, 02 Sep 2025 18:03:07 GMT  
		Size: 20.2 MB (20184048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3738c05c01066b4b3c5c60eb1a38d5c242806ff05a564dbeb0780988211d2e`  
		Last Modified: Tue, 02 Sep 2025 18:03:05 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f0cc63049dd22ff38e3c4352908daa942d16779dcc6849aba6d304a0d57893`  
		Last Modified: Tue, 02 Sep 2025 18:03:06 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fffbe58b304c0ba63911ead2e24a129d537b6c2b9056af7a563e899e5b92a5`  
		Last Modified: Tue, 02 Sep 2025 18:03:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:aa542bf28194a3b9340fad7d9d21ac4736ef0704bf7762c9bba5dc71b9dcc2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2d5bd839942af6fb00666909b372350f63358aaa9641ede37f6ce775db7152`

```dockerfile
```

-	Layers:
	-	`sha256:e6c8638aa86e32883312dae7dcc71bbdada88303e906717bdf6ef9dfd324e013`  
		Last Modified: Tue, 02 Sep 2025 20:07:52 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba0e879ddb8662d6f99807d4b860facac5a85cca52f8a4c1f695483bd4d78adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69913470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0717e48c98453a3eece9de9a628eb9429df463cf90c6f76526e7b6d0fa404df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.4.0-rc.2
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-amd64'; 			sha256='4f5e5a1b6dd0d6ff8476c8def7602d1eeedcb6f602e8dcd45079d352247eba06'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v6'; 			sha256='216ef84b075c270ab2f0bbcf9fcedfb0175226349714a129b7806b4b3f1a460c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v7'; 			sha256='b7184384910ed1b3726f7dc340e3c644640fc5f7028c6ccdfda843cfbcb3fb67'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm64'; 			sha256='e3519d085710d2502c673380f763596ae0b378d0ae8976ccbb14adaed82327ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-ppc64le'; 			sha256='e2bc5c418f680fa7ddb8782eea00a56725189ef672019db62b9f526d120afb08'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-riscv64'; 			sha256='e4f3b40472e3784bf5254eb399aa640205f349ee7c4839db989313d91258b7c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-s390x'; 			sha256='75c24bc03e809ead2e80840280359e3327965c6c1535d0fdc8d48cc86355eecb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Sep 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5be1c5cb61b5158f1dab3ef9e504f10bd421089c0d5ef0e47361f4aab96318`  
		Last Modified: Tue, 02 Sep 2025 18:03:21 GMT  
		Size: 18.4 MB (18406377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4976f6b6daf3107a0649a9d8e9888a7138756d7a0983985f54c0fd0522d86da`  
		Last Modified: Tue, 02 Sep 2025 18:03:26 GMT  
		Size: 20.7 MB (20689980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776a17acfa47d8dcbfc6d05c82a1d1198c52ffe6b422e53cd873fb0478cc6977`  
		Last Modified: Tue, 02 Sep 2025 18:03:22 GMT  
		Size: 20.2 MB (20165955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a76310f78a78338283f4531e0d347de6d8dae369d13d86144ef5770c485b968`  
		Last Modified: Tue, 02 Sep 2025 18:03:19 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34582b9db3bd4a2062cf56a3753c1bf832a35a820912393ded06556716190666`  
		Last Modified: Tue, 02 Sep 2025 18:03:20 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be455ab3af5d18fba88782818edc470301d8332c0019e60c5da945357932603`  
		Last Modified: Tue, 02 Sep 2025 18:03:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:82356f9f9f54e4c15630cfd138704ebbdb5da450fa7feb2637bab9af8419cb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a25a4c967dd36058bbfbb6c5e2e10a156177dc10475c92987f603e9c6f1a7e`

```dockerfile
```

-	Layers:
	-	`sha256:a39b45abd65c3d490de7ccbb39d0eaf6b102061cff97995e869fdf168271e4f1`  
		Last Modified: Tue, 02 Sep 2025 20:07:56 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4631dd946e5d20cade8c516bf30cbd087918fad903beba89ad1a7786f47e2da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71493210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803071019bcd69e517d64ec6583cf72cd70eb3b0a5cb170c7bc3abb191e3e30b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.4.0-rc.2
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-amd64'; 			sha256='4f5e5a1b6dd0d6ff8476c8def7602d1eeedcb6f602e8dcd45079d352247eba06'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v6'; 			sha256='216ef84b075c270ab2f0bbcf9fcedfb0175226349714a129b7806b4b3f1a460c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v7'; 			sha256='b7184384910ed1b3726f7dc340e3c644640fc5f7028c6ccdfda843cfbcb3fb67'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm64'; 			sha256='e3519d085710d2502c673380f763596ae0b378d0ae8976ccbb14adaed82327ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-ppc64le'; 			sha256='e2bc5c418f680fa7ddb8782eea00a56725189ef672019db62b9f526d120afb08'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-riscv64'; 			sha256='e4f3b40472e3784bf5254eb399aa640205f349ee7c4839db989313d91258b7c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-s390x'; 			sha256='75c24bc03e809ead2e80840280359e3327965c6c1535d0fdc8d48cc86355eecb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Tue, 02 Sep 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Sep 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Sep 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76764f4aab4edb3249465d0a29ca57e90f5510642e021dc151b2574132609052`  
		Last Modified: Tue, 02 Sep 2025 18:30:07 GMT  
		Size: 8.2 MB (8217764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d49c866698b852589b12ec80a52435476c941c948a30d1e41af21e126bada86`  
		Last Modified: Tue, 02 Sep 2025 18:30:00 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf302d4b5de7b04892b25784c38cc195e7014acbb0305072c4d18d332b4b49`  
		Last Modified: Tue, 02 Sep 2025 18:30:04 GMT  
		Size: 19.2 MB (19235224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b5bf6ed37d7f9adb5146e95a869cd61ac11a82310d4392156c30598550ac4`  
		Last Modified: Tue, 02 Sep 2025 18:30:07 GMT  
		Size: 20.2 MB (20230145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cbe8c864546ab2f2de16deb5b42b30bd0a78bf11e3540f827b4a064fc4064`  
		Last Modified: Tue, 02 Sep 2025 18:30:02 GMT  
		Size: 19.7 MB (19677173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0f919e7182f0df259bd97ab6b110221c11c2ebf54a9712f5ec4f51f9212b8`  
		Last Modified: Tue, 02 Sep 2025 18:30:01 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5e9bd5ccc7c4504fb931637160b1450ad0f97d826fb74137cdca9b61d814e9`  
		Last Modified: Tue, 02 Sep 2025 18:30:01 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9040e059477347bb2cf174154b44e2a0d6d41f50dc1cf208d5031081b4e1a338`  
		Last Modified: Tue, 02 Sep 2025 18:30:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:cb7859bf3521217d8590853ec15f09439dfa2615c76df6349518be6cb4bed33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335a800bbcdb62dd1d9055d41a06476a4555f81b4d80b429f4b2cc76bb480026`

```dockerfile
```

-	Layers:
	-	`sha256:0b5c35f954d8efb30eb82054be03f943b81d817cfe0f4988100c6a65cda8271c`  
		Last Modified: Tue, 02 Sep 2025 20:08:00 GMT  
		Size: 38.1 KB (38102 bytes)  
		MIME: application/vnd.in-toto+json
