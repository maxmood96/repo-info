<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:20`](#docker20)
-	[`docker:20-dind`](#docker20-dind)
-	[`docker:20-dind-rootless`](#docker20-dind-rootless)
-	[`docker:20-git`](#docker20-git)
-	[`docker:20-windowsservercore`](#docker20-windowsservercore)
-	[`docker:20-windowsservercore-1809`](#docker20-windowsservercore-1809)
-	[`docker:20-windowsservercore-ltsc2022`](#docker20-windowsservercore-ltsc2022)
-	[`docker:20.10`](#docker2010)
-	[`docker:20.10-dind`](#docker2010-dind)
-	[`docker:20.10-dind-rootless`](#docker2010-dind-rootless)
-	[`docker:20.10-git`](#docker2010-git)
-	[`docker:20.10-windowsservercore`](#docker2010-windowsservercore)
-	[`docker:20.10-windowsservercore-1809`](#docker2010-windowsservercore-1809)
-	[`docker:20.10-windowsservercore-ltsc2022`](#docker2010-windowsservercore-ltsc2022)
-	[`docker:20.10.16`](#docker201016)
-	[`docker:20.10.16-alpine3.15`](#docker201016-alpine315)
-	[`docker:20.10.16-dind`](#docker201016-dind)
-	[`docker:20.10.16-dind-alpine3.15`](#docker201016-dind-alpine315)
-	[`docker:20.10.16-dind-rootless`](#docker201016-dind-rootless)
-	[`docker:20.10.16-git`](#docker201016-git)
-	[`docker:20.10.16-windowsservercore`](#docker201016-windowsservercore)
-	[`docker:20.10.16-windowsservercore-1809`](#docker201016-windowsservercore-1809)
-	[`docker:20.10.16-windowsservercore-ltsc2022`](#docker201016-windowsservercore-ltsc2022)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:20`

```console
$ docker pull docker@sha256:bbce511525990d3eb217b0e66d1f437832ebdd28f0ee47ad7f21237424ed9a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:bf1326c676c31156a52c8c971b3b1f2b6b305b738fd7139053843a97205d76a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93858024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452e962280e8dbf51cf3c30175f89815f17c082b1f6c031533cb8f30553dbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e18aeb402936db9a724855ca75c4dde8540fa1f71273aeadb2d3660800403a1e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86081746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ba2f3b7c338f7b9900c78c4605f7ce24d7083f09155221c24eeac44437b973`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:e48027df9b5369763d93050a0029b3c3a6a089f332094f51f8080d2443d940c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:3fb8a736144f844c3903228ad96ba74f7271b33342aa69521d59d904d88205bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100600275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4abd47de51fd416838034c407048ce77c0cfe4cece5a192ee9d20579b0a74c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 12 May 2022 19:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 12 May 2022 19:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 12 May 2022 19:19:49 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:49 GMT
VOLUME [/var/lib/docker]
# Thu, 12 May 2022 19:19:49 GMT
EXPOSE 2375 2376
# Thu, 12 May 2022 19:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 12 May 2022 19:19:49 GMT
CMD []
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c05071a5e9f81830267e0a69c35ed056406786a6a379168ab786bd598aa88`  
		Last Modified: Thu, 12 May 2022 19:20:57 GMT  
		Size: 6.7 MB (6737219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92fafb1edbe6e1b5f0dd97bdeaf519d349c987eac560493fe2982f2423a9ef`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2604faa1ba4171095fbc6fa9d674b95ac8d24171053763ed9661270a14c19851`  
		Last Modified: Thu, 12 May 2022 19:20:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25380f2b2efd2f269ad1706c1ede10d60fbcf2f982db8110dde2173b52e21fa8`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5bc7537e92712bb526f60fed8a26a8f604275cd9991e86c16e2508946ccb7ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92707025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd1505f2e8cc2cb33bbd004024038a207d64bc164d0e4a02784dd6d4ddbd51b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
# Wed, 11 May 2022 00:43:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 May 2022 00:43:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 May 2022 00:43:21 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 11 May 2022 00:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 May 2022 00:43:24 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:24 GMT
VOLUME [/var/lib/docker]
# Wed, 11 May 2022 00:43:25 GMT
EXPOSE 2375 2376
# Wed, 11 May 2022 00:43:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 May 2022 00:43:27 GMT
CMD []
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7787c7635a670bb2a73df457b35cc7189fcb71df87fcebab6a587c6868c1eba9`  
		Last Modified: Wed, 11 May 2022 00:44:59 GMT  
		Size: 6.6 MB (6620287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9929242070a07212fa6187a6481abb7f4f2537de4ca5834dc672eb54aabe985e`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce59cda5df84ca4590a12f295c6e1bdae8b5ab886613f7cb21c8f9981f2ba2a`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe15f5668d48ec3ac87bcfd1153c4f44d21b5932a5b0431b126f12ad38dbd7`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 2.7 KB (2744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:4e3b742acb3afaded351095efc7482921ca0f457245c853ebc066d07e2ce2c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3d8d4b1d6ca4ee26e2efdf7510bc7117a0830c21162670d98a3ba8f1e508b193
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121106963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edffce8b2865900a56304cae05b9a2508e920b32e9696c2b6ccdd490e808b6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 12 May 2022 19:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 12 May 2022 19:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 12 May 2022 19:19:49 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:49 GMT
VOLUME [/var/lib/docker]
# Thu, 12 May 2022 19:19:49 GMT
EXPOSE 2375 2376
# Thu, 12 May 2022 19:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 12 May 2022 19:19:49 GMT
CMD []
# Thu, 12 May 2022 19:19:54 GMT
RUN apk add --no-cache iproute2
# Thu, 12 May 2022 19:19:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 12 May 2022 19:19:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 12 May 2022 19:19:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 12 May 2022 19:19:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 12 May 2022 19:19:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c05071a5e9f81830267e0a69c35ed056406786a6a379168ab786bd598aa88`  
		Last Modified: Thu, 12 May 2022 19:20:57 GMT  
		Size: 6.7 MB (6737219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92fafb1edbe6e1b5f0dd97bdeaf519d349c987eac560493fe2982f2423a9ef`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2604faa1ba4171095fbc6fa9d674b95ac8d24171053763ed9661270a14c19851`  
		Last Modified: Thu, 12 May 2022 19:20:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25380f2b2efd2f269ad1706c1ede10d60fbcf2f982db8110dde2173b52e21fa8`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aab5d3f08f2d4b0d5e44559fabb3acbcd693f9aea6ca28aa48b793cc2464fb9`  
		Last Modified: Thu, 12 May 2022 19:21:16 GMT  
		Size: 1.2 MB (1161996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949acbcf253f9553e99a99f78d554f956229d20fec09a375ee6ec4527c1be37`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676a4d127421e7ec39bc0565e9ede81698d27f15aebb10f1f359c8fb2b15801`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7d93c2910d4af089c4d67b58540e996cf217ed72781b3d51a81870854d86a7`  
		Last Modified: Thu, 12 May 2022 19:21:19 GMT  
		Size: 19.3 MB (19342976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e5c5117ec29177e7bbf18009d31a033f3044edd9d5dc9d67a9fd7e4d9a7a5f`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86bdf6636db6a8b06847ac84644c7d50300c2955b2b200ce3aa55f3074ebecd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115065045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6f1e988d89dd418bf82197674b0e012f1aece1514f899a6397dd8a544668e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
# Wed, 11 May 2022 00:43:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 May 2022 00:43:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 May 2022 00:43:21 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 11 May 2022 00:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 May 2022 00:43:24 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:24 GMT
VOLUME [/var/lib/docker]
# Wed, 11 May 2022 00:43:25 GMT
EXPOSE 2375 2376
# Wed, 11 May 2022 00:43:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 May 2022 00:43:27 GMT
CMD []
# Wed, 11 May 2022 00:43:36 GMT
RUN apk add --no-cache iproute2
# Wed, 11 May 2022 00:43:36 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 May 2022 00:43:37 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 May 2022 00:43:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 11 May 2022 00:43:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 May 2022 00:43:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 May 2022 00:43:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7787c7635a670bb2a73df457b35cc7189fcb71df87fcebab6a587c6868c1eba9`  
		Last Modified: Wed, 11 May 2022 00:44:59 GMT  
		Size: 6.6 MB (6620287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9929242070a07212fa6187a6481abb7f4f2537de4ca5834dc672eb54aabe985e`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce59cda5df84ca4590a12f295c6e1bdae8b5ab886613f7cb21c8f9981f2ba2a`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe15f5668d48ec3ac87bcfd1153c4f44d21b5932a5b0431b126f12ad38dbd7`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 2.7 KB (2744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b3985e0ad4d291eea7cf874cc318605bcf5da8770d51f4b65555611d8ec1cd`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 1.2 MB (1177961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7d124f6c1ceea4201be7da76786410ebeebbc1ca0754d98f312a30c3d9421f`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1273b4a7d40bb74302f237cb53eb0bcc54444ca383e15e5d33b3d060b5f98dd1`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2a3f703dc20a84ab20a7a95730da6579aac72a8c58bc0d24929d8617dc634c`  
		Last Modified: Wed, 11 May 2022 00:45:25 GMT  
		Size: 21.2 MB (21178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66854ad6b8b792204d375a5f73dd9da3f91f4ef4bca9cce17479a18a62843ce8`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:9c2f06da21a09a51e1c32a0b19068ef37a2ee1ca01e0fcbcf49ba912616e792d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:09a6f8585fc77b3f62ff088cd2d1c9bc8808bf8eec20f95acd5cc122b547892f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100683328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a153898ad6882b35217ab25274ce23450c2ac8fee9d45562ef8261ea1a6e7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:20:02 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41802dad92c51d059b856984d49e518b446feee98f83edf120d1ad2a607850cc`  
		Last Modified: Thu, 12 May 2022 19:21:42 GMT  
		Size: 6.8 MB (6825304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6408bd6587f86e51d8b510824e4d02f9234b12596cfe9a6c4d1f992bfb4c982a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93017466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db57e40fdd155aef868beef5df895c1cac8a30a2b93dd69ef4fd363fe3daaa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
# Wed, 11 May 2022 00:43:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed14c2edfc4c1e09a3dc29020e19fad2d064256d93ffbc664d1f2a35beca119`  
		Last Modified: Wed, 11 May 2022 00:45:48 GMT  
		Size: 6.9 MB (6935720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:44251ae4b6e381ac726b35292cd0cedc2c9273e3b83991b56eca7290f59ee4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.707; amd64
	-	windows version 10.0.17763.2928; amd64

### `docker:20-windowsservercore` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:d63c51f65add3dd63c6d57455a72eda503f74a3d8b382c7b847942f75efdc12c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290667395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e6fc2818e4a6b2961fbf12c81c442c94666e05812a63248a527d57d0605c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:00 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:16:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9698df5d87653df3e05322abc936eba7b08b4ac1e1531d300326f852acb560d`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea315f146ff5d08a865f8afe9f6b3abbc0fbe3254d7c658afd18f2c6a6916c3`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c801fe2ce56a50e273ce72ad681cab5b3aff867063f17ed4a285d1d11f33e6`  
		Last Modified: Thu, 12 May 2022 19:19:40 GMT  
		Size: 52.5 MB (52523408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull docker@sha256:d91fe2d69d9526fb466c37afa1a7c5c14b3449caa82ead5ae8d88f081a98b8e7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556871108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963abf2508f0bb0b3f5da00f2a354a0c74d867eaabd99877b24cc991a6c99be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:17:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:53 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b919bb58ec3ed41b7e2e67e75497f0619d0f5ffa4ed0bf076d25d167186aed5`  
		Last Modified: Wed, 11 May 2022 01:19:58 GMT  
		Size: 486.0 KB (486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17963b29ee9a8eb140f806106b868925eef0ec9b9b9b7530399e44aa39644831`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794437e928236733907f6be03a38e33807049ff42b8df4f81f2585ce98a5cd`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fec92946e098247270b24628d39d2599af778a0f46841732c2d6180065fc43`  
		Last Modified: Thu, 12 May 2022 19:20:52 GMT  
		Size: 52.3 MB (52324957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:4298f49bbd424c400dc5d6e9f78f9710dc2abdde78924e61ec48bf4d10b649f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull docker@sha256:d91fe2d69d9526fb466c37afa1a7c5c14b3449caa82ead5ae8d88f081a98b8e7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556871108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963abf2508f0bb0b3f5da00f2a354a0c74d867eaabd99877b24cc991a6c99be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:17:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:53 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b919bb58ec3ed41b7e2e67e75497f0619d0f5ffa4ed0bf076d25d167186aed5`  
		Last Modified: Wed, 11 May 2022 01:19:58 GMT  
		Size: 486.0 KB (486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17963b29ee9a8eb140f806106b868925eef0ec9b9b9b7530399e44aa39644831`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794437e928236733907f6be03a38e33807049ff42b8df4f81f2585ce98a5cd`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fec92946e098247270b24628d39d2599af778a0f46841732c2d6180065fc43`  
		Last Modified: Thu, 12 May 2022 19:20:52 GMT  
		Size: 52.3 MB (52324957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:025608dd7c48461a51e36543342256af22b1bc5933f311d3774503c2eaacd05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `docker:20-windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:d63c51f65add3dd63c6d57455a72eda503f74a3d8b382c7b847942f75efdc12c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290667395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e6fc2818e4a6b2961fbf12c81c442c94666e05812a63248a527d57d0605c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:00 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:16:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9698df5d87653df3e05322abc936eba7b08b4ac1e1531d300326f852acb560d`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea315f146ff5d08a865f8afe9f6b3abbc0fbe3254d7c658afd18f2c6a6916c3`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c801fe2ce56a50e273ce72ad681cab5b3aff867063f17ed4a285d1d11f33e6`  
		Last Modified: Thu, 12 May 2022 19:19:40 GMT  
		Size: 52.5 MB (52523408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:bbce511525990d3eb217b0e66d1f437832ebdd28f0ee47ad7f21237424ed9a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:bf1326c676c31156a52c8c971b3b1f2b6b305b738fd7139053843a97205d76a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93858024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452e962280e8dbf51cf3c30175f89815f17c082b1f6c031533cb8f30553dbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e18aeb402936db9a724855ca75c4dde8540fa1f71273aeadb2d3660800403a1e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86081746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ba2f3b7c338f7b9900c78c4605f7ce24d7083f09155221c24eeac44437b973`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:e48027df9b5369763d93050a0029b3c3a6a089f332094f51f8080d2443d940c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:3fb8a736144f844c3903228ad96ba74f7271b33342aa69521d59d904d88205bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100600275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4abd47de51fd416838034c407048ce77c0cfe4cece5a192ee9d20579b0a74c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 12 May 2022 19:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 12 May 2022 19:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 12 May 2022 19:19:49 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:49 GMT
VOLUME [/var/lib/docker]
# Thu, 12 May 2022 19:19:49 GMT
EXPOSE 2375 2376
# Thu, 12 May 2022 19:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 12 May 2022 19:19:49 GMT
CMD []
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c05071a5e9f81830267e0a69c35ed056406786a6a379168ab786bd598aa88`  
		Last Modified: Thu, 12 May 2022 19:20:57 GMT  
		Size: 6.7 MB (6737219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92fafb1edbe6e1b5f0dd97bdeaf519d349c987eac560493fe2982f2423a9ef`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2604faa1ba4171095fbc6fa9d674b95ac8d24171053763ed9661270a14c19851`  
		Last Modified: Thu, 12 May 2022 19:20:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25380f2b2efd2f269ad1706c1ede10d60fbcf2f982db8110dde2173b52e21fa8`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5bc7537e92712bb526f60fed8a26a8f604275cd9991e86c16e2508946ccb7ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92707025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd1505f2e8cc2cb33bbd004024038a207d64bc164d0e4a02784dd6d4ddbd51b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
# Wed, 11 May 2022 00:43:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 May 2022 00:43:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 May 2022 00:43:21 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 11 May 2022 00:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 May 2022 00:43:24 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:24 GMT
VOLUME [/var/lib/docker]
# Wed, 11 May 2022 00:43:25 GMT
EXPOSE 2375 2376
# Wed, 11 May 2022 00:43:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 May 2022 00:43:27 GMT
CMD []
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7787c7635a670bb2a73df457b35cc7189fcb71df87fcebab6a587c6868c1eba9`  
		Last Modified: Wed, 11 May 2022 00:44:59 GMT  
		Size: 6.6 MB (6620287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9929242070a07212fa6187a6481abb7f4f2537de4ca5834dc672eb54aabe985e`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce59cda5df84ca4590a12f295c6e1bdae8b5ab886613f7cb21c8f9981f2ba2a`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe15f5668d48ec3ac87bcfd1153c4f44d21b5932a5b0431b126f12ad38dbd7`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 2.7 KB (2744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:4e3b742acb3afaded351095efc7482921ca0f457245c853ebc066d07e2ce2c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3d8d4b1d6ca4ee26e2efdf7510bc7117a0830c21162670d98a3ba8f1e508b193
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121106963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edffce8b2865900a56304cae05b9a2508e920b32e9696c2b6ccdd490e808b6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 12 May 2022 19:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 12 May 2022 19:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 12 May 2022 19:19:49 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:49 GMT
VOLUME [/var/lib/docker]
# Thu, 12 May 2022 19:19:49 GMT
EXPOSE 2375 2376
# Thu, 12 May 2022 19:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 12 May 2022 19:19:49 GMT
CMD []
# Thu, 12 May 2022 19:19:54 GMT
RUN apk add --no-cache iproute2
# Thu, 12 May 2022 19:19:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 12 May 2022 19:19:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 12 May 2022 19:19:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 12 May 2022 19:19:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 12 May 2022 19:19:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c05071a5e9f81830267e0a69c35ed056406786a6a379168ab786bd598aa88`  
		Last Modified: Thu, 12 May 2022 19:20:57 GMT  
		Size: 6.7 MB (6737219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92fafb1edbe6e1b5f0dd97bdeaf519d349c987eac560493fe2982f2423a9ef`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2604faa1ba4171095fbc6fa9d674b95ac8d24171053763ed9661270a14c19851`  
		Last Modified: Thu, 12 May 2022 19:20:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25380f2b2efd2f269ad1706c1ede10d60fbcf2f982db8110dde2173b52e21fa8`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aab5d3f08f2d4b0d5e44559fabb3acbcd693f9aea6ca28aa48b793cc2464fb9`  
		Last Modified: Thu, 12 May 2022 19:21:16 GMT  
		Size: 1.2 MB (1161996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949acbcf253f9553e99a99f78d554f956229d20fec09a375ee6ec4527c1be37`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676a4d127421e7ec39bc0565e9ede81698d27f15aebb10f1f359c8fb2b15801`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7d93c2910d4af089c4d67b58540e996cf217ed72781b3d51a81870854d86a7`  
		Last Modified: Thu, 12 May 2022 19:21:19 GMT  
		Size: 19.3 MB (19342976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e5c5117ec29177e7bbf18009d31a033f3044edd9d5dc9d67a9fd7e4d9a7a5f`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86bdf6636db6a8b06847ac84644c7d50300c2955b2b200ce3aa55f3074ebecd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115065045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6f1e988d89dd418bf82197674b0e012f1aece1514f899a6397dd8a544668e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
# Wed, 11 May 2022 00:43:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 May 2022 00:43:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 May 2022 00:43:21 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 11 May 2022 00:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 May 2022 00:43:24 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:24 GMT
VOLUME [/var/lib/docker]
# Wed, 11 May 2022 00:43:25 GMT
EXPOSE 2375 2376
# Wed, 11 May 2022 00:43:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 May 2022 00:43:27 GMT
CMD []
# Wed, 11 May 2022 00:43:36 GMT
RUN apk add --no-cache iproute2
# Wed, 11 May 2022 00:43:36 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 May 2022 00:43:37 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 May 2022 00:43:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 11 May 2022 00:43:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 May 2022 00:43:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 May 2022 00:43:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7787c7635a670bb2a73df457b35cc7189fcb71df87fcebab6a587c6868c1eba9`  
		Last Modified: Wed, 11 May 2022 00:44:59 GMT  
		Size: 6.6 MB (6620287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9929242070a07212fa6187a6481abb7f4f2537de4ca5834dc672eb54aabe985e`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce59cda5df84ca4590a12f295c6e1bdae8b5ab886613f7cb21c8f9981f2ba2a`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe15f5668d48ec3ac87bcfd1153c4f44d21b5932a5b0431b126f12ad38dbd7`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 2.7 KB (2744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b3985e0ad4d291eea7cf874cc318605bcf5da8770d51f4b65555611d8ec1cd`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 1.2 MB (1177961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7d124f6c1ceea4201be7da76786410ebeebbc1ca0754d98f312a30c3d9421f`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1273b4a7d40bb74302f237cb53eb0bcc54444ca383e15e5d33b3d060b5f98dd1`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2a3f703dc20a84ab20a7a95730da6579aac72a8c58bc0d24929d8617dc634c`  
		Last Modified: Wed, 11 May 2022 00:45:25 GMT  
		Size: 21.2 MB (21178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66854ad6b8b792204d375a5f73dd9da3f91f4ef4bca9cce17479a18a62843ce8`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:9c2f06da21a09a51e1c32a0b19068ef37a2ee1ca01e0fcbcf49ba912616e792d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:09a6f8585fc77b3f62ff088cd2d1c9bc8808bf8eec20f95acd5cc122b547892f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100683328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a153898ad6882b35217ab25274ce23450c2ac8fee9d45562ef8261ea1a6e7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:20:02 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41802dad92c51d059b856984d49e518b446feee98f83edf120d1ad2a607850cc`  
		Last Modified: Thu, 12 May 2022 19:21:42 GMT  
		Size: 6.8 MB (6825304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6408bd6587f86e51d8b510824e4d02f9234b12596cfe9a6c4d1f992bfb4c982a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93017466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db57e40fdd155aef868beef5df895c1cac8a30a2b93dd69ef4fd363fe3daaa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
# Wed, 11 May 2022 00:43:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed14c2edfc4c1e09a3dc29020e19fad2d064256d93ffbc664d1f2a35beca119`  
		Last Modified: Wed, 11 May 2022 00:45:48 GMT  
		Size: 6.9 MB (6935720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:44251ae4b6e381ac726b35292cd0cedc2c9273e3b83991b56eca7290f59ee4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.707; amd64
	-	windows version 10.0.17763.2928; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:d63c51f65add3dd63c6d57455a72eda503f74a3d8b382c7b847942f75efdc12c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290667395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e6fc2818e4a6b2961fbf12c81c442c94666e05812a63248a527d57d0605c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:00 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:16:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9698df5d87653df3e05322abc936eba7b08b4ac1e1531d300326f852acb560d`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea315f146ff5d08a865f8afe9f6b3abbc0fbe3254d7c658afd18f2c6a6916c3`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c801fe2ce56a50e273ce72ad681cab5b3aff867063f17ed4a285d1d11f33e6`  
		Last Modified: Thu, 12 May 2022 19:19:40 GMT  
		Size: 52.5 MB (52523408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull docker@sha256:d91fe2d69d9526fb466c37afa1a7c5c14b3449caa82ead5ae8d88f081a98b8e7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556871108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963abf2508f0bb0b3f5da00f2a354a0c74d867eaabd99877b24cc991a6c99be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:17:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:53 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b919bb58ec3ed41b7e2e67e75497f0619d0f5ffa4ed0bf076d25d167186aed5`  
		Last Modified: Wed, 11 May 2022 01:19:58 GMT  
		Size: 486.0 KB (486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17963b29ee9a8eb140f806106b868925eef0ec9b9b9b7530399e44aa39644831`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794437e928236733907f6be03a38e33807049ff42b8df4f81f2585ce98a5cd`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fec92946e098247270b24628d39d2599af778a0f46841732c2d6180065fc43`  
		Last Modified: Thu, 12 May 2022 19:20:52 GMT  
		Size: 52.3 MB (52324957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:4298f49bbd424c400dc5d6e9f78f9710dc2abdde78924e61ec48bf4d10b649f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull docker@sha256:d91fe2d69d9526fb466c37afa1a7c5c14b3449caa82ead5ae8d88f081a98b8e7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556871108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963abf2508f0bb0b3f5da00f2a354a0c74d867eaabd99877b24cc991a6c99be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:17:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:53 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b919bb58ec3ed41b7e2e67e75497f0619d0f5ffa4ed0bf076d25d167186aed5`  
		Last Modified: Wed, 11 May 2022 01:19:58 GMT  
		Size: 486.0 KB (486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17963b29ee9a8eb140f806106b868925eef0ec9b9b9b7530399e44aa39644831`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794437e928236733907f6be03a38e33807049ff42b8df4f81f2585ce98a5cd`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fec92946e098247270b24628d39d2599af778a0f46841732c2d6180065fc43`  
		Last Modified: Thu, 12 May 2022 19:20:52 GMT  
		Size: 52.3 MB (52324957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:025608dd7c48461a51e36543342256af22b1bc5933f311d3774503c2eaacd05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `docker:20.10-windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:d63c51f65add3dd63c6d57455a72eda503f74a3d8b382c7b847942f75efdc12c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290667395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e6fc2818e4a6b2961fbf12c81c442c94666e05812a63248a527d57d0605c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:00 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:16:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9698df5d87653df3e05322abc936eba7b08b4ac1e1531d300326f852acb560d`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea315f146ff5d08a865f8afe9f6b3abbc0fbe3254d7c658afd18f2c6a6916c3`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c801fe2ce56a50e273ce72ad681cab5b3aff867063f17ed4a285d1d11f33e6`  
		Last Modified: Thu, 12 May 2022 19:19:40 GMT  
		Size: 52.5 MB (52523408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.16`

```console
$ docker pull docker@sha256:c139e5832b01db9f54ceec3a401ed053b22100a80cb0273395d958b64085aad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `docker:20.10.16` - linux; amd64

```console
$ docker pull docker@sha256:bf1326c676c31156a52c8c971b3b1f2b6b305b738fd7139053843a97205d76a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93858024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452e962280e8dbf51cf3c30175f89815f17c082b1f6c031533cb8f30553dbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.16-alpine3.15`

```console
$ docker pull docker@sha256:c139e5832b01db9f54ceec3a401ed053b22100a80cb0273395d958b64085aad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `docker:20.10.16-alpine3.15` - linux; amd64

```console
$ docker pull docker@sha256:bf1326c676c31156a52c8c971b3b1f2b6b305b738fd7139053843a97205d76a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93858024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452e962280e8dbf51cf3c30175f89815f17c082b1f6c031533cb8f30553dbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.16-dind`

```console
$ docker pull docker@sha256:1d9a004b65f18e9f6b478e074f73fd667f6c6538a5c9bab14e33e41996699c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `docker:20.10.16-dind` - linux; amd64

```console
$ docker pull docker@sha256:3fb8a736144f844c3903228ad96ba74f7271b33342aa69521d59d904d88205bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100600275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4abd47de51fd416838034c407048ce77c0cfe4cece5a192ee9d20579b0a74c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 12 May 2022 19:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 12 May 2022 19:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 12 May 2022 19:19:49 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:49 GMT
VOLUME [/var/lib/docker]
# Thu, 12 May 2022 19:19:49 GMT
EXPOSE 2375 2376
# Thu, 12 May 2022 19:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 12 May 2022 19:19:49 GMT
CMD []
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c05071a5e9f81830267e0a69c35ed056406786a6a379168ab786bd598aa88`  
		Last Modified: Thu, 12 May 2022 19:20:57 GMT  
		Size: 6.7 MB (6737219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92fafb1edbe6e1b5f0dd97bdeaf519d349c987eac560493fe2982f2423a9ef`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2604faa1ba4171095fbc6fa9d674b95ac8d24171053763ed9661270a14c19851`  
		Last Modified: Thu, 12 May 2022 19:20:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25380f2b2efd2f269ad1706c1ede10d60fbcf2f982db8110dde2173b52e21fa8`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.16-dind-alpine3.15`

```console
$ docker pull docker@sha256:1d9a004b65f18e9f6b478e074f73fd667f6c6538a5c9bab14e33e41996699c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `docker:20.10.16-dind-alpine3.15` - linux; amd64

```console
$ docker pull docker@sha256:3fb8a736144f844c3903228ad96ba74f7271b33342aa69521d59d904d88205bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100600275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4abd47de51fd416838034c407048ce77c0cfe4cece5a192ee9d20579b0a74c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 12 May 2022 19:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 12 May 2022 19:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 12 May 2022 19:19:49 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:49 GMT
VOLUME [/var/lib/docker]
# Thu, 12 May 2022 19:19:49 GMT
EXPOSE 2375 2376
# Thu, 12 May 2022 19:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 12 May 2022 19:19:49 GMT
CMD []
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c05071a5e9f81830267e0a69c35ed056406786a6a379168ab786bd598aa88`  
		Last Modified: Thu, 12 May 2022 19:20:57 GMT  
		Size: 6.7 MB (6737219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92fafb1edbe6e1b5f0dd97bdeaf519d349c987eac560493fe2982f2423a9ef`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2604faa1ba4171095fbc6fa9d674b95ac8d24171053763ed9661270a14c19851`  
		Last Modified: Thu, 12 May 2022 19:20:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25380f2b2efd2f269ad1706c1ede10d60fbcf2f982db8110dde2173b52e21fa8`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.16-dind-rootless`

```console
$ docker pull docker@sha256:8fe4511d2bdebe716984f4b158aae3c9402d6106f13ee2e9634a884b8045051b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `docker:20.10.16-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3d8d4b1d6ca4ee26e2efdf7510bc7117a0830c21162670d98a3ba8f1e508b193
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121106963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edffce8b2865900a56304cae05b9a2508e920b32e9696c2b6ccdd490e808b6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 12 May 2022 19:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 12 May 2022 19:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 12 May 2022 19:19:49 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:49 GMT
VOLUME [/var/lib/docker]
# Thu, 12 May 2022 19:19:49 GMT
EXPOSE 2375 2376
# Thu, 12 May 2022 19:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 12 May 2022 19:19:49 GMT
CMD []
# Thu, 12 May 2022 19:19:54 GMT
RUN apk add --no-cache iproute2
# Thu, 12 May 2022 19:19:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 12 May 2022 19:19:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 12 May 2022 19:19:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 12 May 2022 19:19:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 12 May 2022 19:19:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c05071a5e9f81830267e0a69c35ed056406786a6a379168ab786bd598aa88`  
		Last Modified: Thu, 12 May 2022 19:20:57 GMT  
		Size: 6.7 MB (6737219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92fafb1edbe6e1b5f0dd97bdeaf519d349c987eac560493fe2982f2423a9ef`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2604faa1ba4171095fbc6fa9d674b95ac8d24171053763ed9661270a14c19851`  
		Last Modified: Thu, 12 May 2022 19:20:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25380f2b2efd2f269ad1706c1ede10d60fbcf2f982db8110dde2173b52e21fa8`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aab5d3f08f2d4b0d5e44559fabb3acbcd693f9aea6ca28aa48b793cc2464fb9`  
		Last Modified: Thu, 12 May 2022 19:21:16 GMT  
		Size: 1.2 MB (1161996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949acbcf253f9553e99a99f78d554f956229d20fec09a375ee6ec4527c1be37`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676a4d127421e7ec39bc0565e9ede81698d27f15aebb10f1f359c8fb2b15801`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7d93c2910d4af089c4d67b58540e996cf217ed72781b3d51a81870854d86a7`  
		Last Modified: Thu, 12 May 2022 19:21:19 GMT  
		Size: 19.3 MB (19342976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e5c5117ec29177e7bbf18009d31a033f3044edd9d5dc9d67a9fd7e4d9a7a5f`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.16-git`

```console
$ docker pull docker@sha256:614faacfb51edfd42fb4190c1fd084f0d40e4d1ab4144294685499dadd2f5401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `docker:20.10.16-git` - linux; amd64

```console
$ docker pull docker@sha256:09a6f8585fc77b3f62ff088cd2d1c9bc8808bf8eec20f95acd5cc122b547892f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100683328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a153898ad6882b35217ab25274ce23450c2ac8fee9d45562ef8261ea1a6e7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:20:02 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41802dad92c51d059b856984d49e518b446feee98f83edf120d1ad2a607850cc`  
		Last Modified: Thu, 12 May 2022 19:21:42 GMT  
		Size: 6.8 MB (6825304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.16-windowsservercore`

```console
$ docker pull docker@sha256:44251ae4b6e381ac726b35292cd0cedc2c9273e3b83991b56eca7290f59ee4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.707; amd64
	-	windows version 10.0.17763.2928; amd64

### `docker:20.10.16-windowsservercore` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:d63c51f65add3dd63c6d57455a72eda503f74a3d8b382c7b847942f75efdc12c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290667395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e6fc2818e4a6b2961fbf12c81c442c94666e05812a63248a527d57d0605c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:00 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:16:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9698df5d87653df3e05322abc936eba7b08b4ac1e1531d300326f852acb560d`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea315f146ff5d08a865f8afe9f6b3abbc0fbe3254d7c658afd18f2c6a6916c3`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c801fe2ce56a50e273ce72ad681cab5b3aff867063f17ed4a285d1d11f33e6`  
		Last Modified: Thu, 12 May 2022 19:19:40 GMT  
		Size: 52.5 MB (52523408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.16-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull docker@sha256:d91fe2d69d9526fb466c37afa1a7c5c14b3449caa82ead5ae8d88f081a98b8e7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556871108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963abf2508f0bb0b3f5da00f2a354a0c74d867eaabd99877b24cc991a6c99be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:17:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:53 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b919bb58ec3ed41b7e2e67e75497f0619d0f5ffa4ed0bf076d25d167186aed5`  
		Last Modified: Wed, 11 May 2022 01:19:58 GMT  
		Size: 486.0 KB (486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17963b29ee9a8eb140f806106b868925eef0ec9b9b9b7530399e44aa39644831`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794437e928236733907f6be03a38e33807049ff42b8df4f81f2585ce98a5cd`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fec92946e098247270b24628d39d2599af778a0f46841732c2d6180065fc43`  
		Last Modified: Thu, 12 May 2022 19:20:52 GMT  
		Size: 52.3 MB (52324957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.16-windowsservercore-1809`

```console
$ docker pull docker@sha256:4298f49bbd424c400dc5d6e9f78f9710dc2abdde78924e61ec48bf4d10b649f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `docker:20.10.16-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull docker@sha256:d91fe2d69d9526fb466c37afa1a7c5c14b3449caa82ead5ae8d88f081a98b8e7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556871108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963abf2508f0bb0b3f5da00f2a354a0c74d867eaabd99877b24cc991a6c99be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:17:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:53 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b919bb58ec3ed41b7e2e67e75497f0619d0f5ffa4ed0bf076d25d167186aed5`  
		Last Modified: Wed, 11 May 2022 01:19:58 GMT  
		Size: 486.0 KB (486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17963b29ee9a8eb140f806106b868925eef0ec9b9b9b7530399e44aa39644831`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794437e928236733907f6be03a38e33807049ff42b8df4f81f2585ce98a5cd`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fec92946e098247270b24628d39d2599af778a0f46841732c2d6180065fc43`  
		Last Modified: Thu, 12 May 2022 19:20:52 GMT  
		Size: 52.3 MB (52324957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.16-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:025608dd7c48461a51e36543342256af22b1bc5933f311d3774503c2eaacd05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `docker:20.10.16-windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:d63c51f65add3dd63c6d57455a72eda503f74a3d8b382c7b847942f75efdc12c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290667395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e6fc2818e4a6b2961fbf12c81c442c94666e05812a63248a527d57d0605c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:00 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:16:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9698df5d87653df3e05322abc936eba7b08b4ac1e1531d300326f852acb560d`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea315f146ff5d08a865f8afe9f6b3abbc0fbe3254d7c658afd18f2c6a6916c3`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c801fe2ce56a50e273ce72ad681cab5b3aff867063f17ed4a285d1d11f33e6`  
		Last Modified: Thu, 12 May 2022 19:19:40 GMT  
		Size: 52.5 MB (52523408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:e48027df9b5369763d93050a0029b3c3a6a089f332094f51f8080d2443d940c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:3fb8a736144f844c3903228ad96ba74f7271b33342aa69521d59d904d88205bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100600275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4abd47de51fd416838034c407048ce77c0cfe4cece5a192ee9d20579b0a74c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 12 May 2022 19:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 12 May 2022 19:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 12 May 2022 19:19:49 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:49 GMT
VOLUME [/var/lib/docker]
# Thu, 12 May 2022 19:19:49 GMT
EXPOSE 2375 2376
# Thu, 12 May 2022 19:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 12 May 2022 19:19:49 GMT
CMD []
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c05071a5e9f81830267e0a69c35ed056406786a6a379168ab786bd598aa88`  
		Last Modified: Thu, 12 May 2022 19:20:57 GMT  
		Size: 6.7 MB (6737219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92fafb1edbe6e1b5f0dd97bdeaf519d349c987eac560493fe2982f2423a9ef`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2604faa1ba4171095fbc6fa9d674b95ac8d24171053763ed9661270a14c19851`  
		Last Modified: Thu, 12 May 2022 19:20:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25380f2b2efd2f269ad1706c1ede10d60fbcf2f982db8110dde2173b52e21fa8`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5bc7537e92712bb526f60fed8a26a8f604275cd9991e86c16e2508946ccb7ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92707025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd1505f2e8cc2cb33bbd004024038a207d64bc164d0e4a02784dd6d4ddbd51b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
# Wed, 11 May 2022 00:43:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 May 2022 00:43:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 May 2022 00:43:21 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 11 May 2022 00:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 May 2022 00:43:24 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:24 GMT
VOLUME [/var/lib/docker]
# Wed, 11 May 2022 00:43:25 GMT
EXPOSE 2375 2376
# Wed, 11 May 2022 00:43:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 May 2022 00:43:27 GMT
CMD []
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7787c7635a670bb2a73df457b35cc7189fcb71df87fcebab6a587c6868c1eba9`  
		Last Modified: Wed, 11 May 2022 00:44:59 GMT  
		Size: 6.6 MB (6620287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9929242070a07212fa6187a6481abb7f4f2537de4ca5834dc672eb54aabe985e`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce59cda5df84ca4590a12f295c6e1bdae8b5ab886613f7cb21c8f9981f2ba2a`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe15f5668d48ec3ac87bcfd1153c4f44d21b5932a5b0431b126f12ad38dbd7`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 2.7 KB (2744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:4e3b742acb3afaded351095efc7482921ca0f457245c853ebc066d07e2ce2c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3d8d4b1d6ca4ee26e2efdf7510bc7117a0830c21162670d98a3ba8f1e508b193
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121106963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edffce8b2865900a56304cae05b9a2508e920b32e9696c2b6ccdd490e808b6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 12 May 2022 19:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 12 May 2022 19:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 12 May 2022 19:19:49 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:49 GMT
VOLUME [/var/lib/docker]
# Thu, 12 May 2022 19:19:49 GMT
EXPOSE 2375 2376
# Thu, 12 May 2022 19:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 12 May 2022 19:19:49 GMT
CMD []
# Thu, 12 May 2022 19:19:54 GMT
RUN apk add --no-cache iproute2
# Thu, 12 May 2022 19:19:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 12 May 2022 19:19:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 12 May 2022 19:19:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 12 May 2022 19:19:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 12 May 2022 19:19:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 12 May 2022 19:19:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c05071a5e9f81830267e0a69c35ed056406786a6a379168ab786bd598aa88`  
		Last Modified: Thu, 12 May 2022 19:20:57 GMT  
		Size: 6.7 MB (6737219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92fafb1edbe6e1b5f0dd97bdeaf519d349c987eac560493fe2982f2423a9ef`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2604faa1ba4171095fbc6fa9d674b95ac8d24171053763ed9661270a14c19851`  
		Last Modified: Thu, 12 May 2022 19:20:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25380f2b2efd2f269ad1706c1ede10d60fbcf2f982db8110dde2173b52e21fa8`  
		Last Modified: Thu, 12 May 2022 19:20:56 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aab5d3f08f2d4b0d5e44559fabb3acbcd693f9aea6ca28aa48b793cc2464fb9`  
		Last Modified: Thu, 12 May 2022 19:21:16 GMT  
		Size: 1.2 MB (1161996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949acbcf253f9553e99a99f78d554f956229d20fec09a375ee6ec4527c1be37`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676a4d127421e7ec39bc0565e9ede81698d27f15aebb10f1f359c8fb2b15801`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7d93c2910d4af089c4d67b58540e996cf217ed72781b3d51a81870854d86a7`  
		Last Modified: Thu, 12 May 2022 19:21:19 GMT  
		Size: 19.3 MB (19342976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e5c5117ec29177e7bbf18009d31a033f3044edd9d5dc9d67a9fd7e4d9a7a5f`  
		Last Modified: Thu, 12 May 2022 19:21:15 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86bdf6636db6a8b06847ac84644c7d50300c2955b2b200ce3aa55f3074ebecd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115065045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6f1e988d89dd418bf82197674b0e012f1aece1514f899a6397dd8a544668e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
# Wed, 11 May 2022 00:43:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 May 2022 00:43:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 May 2022 00:43:21 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 11 May 2022 00:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 May 2022 00:43:24 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:24 GMT
VOLUME [/var/lib/docker]
# Wed, 11 May 2022 00:43:25 GMT
EXPOSE 2375 2376
# Wed, 11 May 2022 00:43:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 May 2022 00:43:27 GMT
CMD []
# Wed, 11 May 2022 00:43:36 GMT
RUN apk add --no-cache iproute2
# Wed, 11 May 2022 00:43:36 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 May 2022 00:43:37 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 May 2022 00:43:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 11 May 2022 00:43:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 May 2022 00:43:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 May 2022 00:43:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7787c7635a670bb2a73df457b35cc7189fcb71df87fcebab6a587c6868c1eba9`  
		Last Modified: Wed, 11 May 2022 00:44:59 GMT  
		Size: 6.6 MB (6620287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9929242070a07212fa6187a6481abb7f4f2537de4ca5834dc672eb54aabe985e`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce59cda5df84ca4590a12f295c6e1bdae8b5ab886613f7cb21c8f9981f2ba2a`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe15f5668d48ec3ac87bcfd1153c4f44d21b5932a5b0431b126f12ad38dbd7`  
		Last Modified: Wed, 11 May 2022 00:44:58 GMT  
		Size: 2.7 KB (2744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b3985e0ad4d291eea7cf874cc318605bcf5da8770d51f4b65555611d8ec1cd`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 1.2 MB (1177961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7d124f6c1ceea4201be7da76786410ebeebbc1ca0754d98f312a30c3d9421f`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1273b4a7d40bb74302f237cb53eb0bcc54444ca383e15e5d33b3d060b5f98dd1`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2a3f703dc20a84ab20a7a95730da6579aac72a8c58bc0d24929d8617dc634c`  
		Last Modified: Wed, 11 May 2022 00:45:25 GMT  
		Size: 21.2 MB (21178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66854ad6b8b792204d375a5f73dd9da3f91f4ef4bca9cce17479a18a62843ce8`  
		Last Modified: Wed, 11 May 2022 00:45:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:9c2f06da21a09a51e1c32a0b19068ef37a2ee1ca01e0fcbcf49ba912616e792d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:09a6f8585fc77b3f62ff088cd2d1c9bc8808bf8eec20f95acd5cc122b547892f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100683328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a153898ad6882b35217ab25274ce23450c2ac8fee9d45562ef8261ea1a6e7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
# Thu, 12 May 2022 19:20:02 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41802dad92c51d059b856984d49e518b446feee98f83edf120d1ad2a607850cc`  
		Last Modified: Thu, 12 May 2022 19:21:42 GMT  
		Size: 6.8 MB (6825304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6408bd6587f86e51d8b510824e4d02f9234b12596cfe9a6c4d1f992bfb4c982a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93017466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db57e40fdd155aef868beef5df895c1cac8a30a2b93dd69ef4fd363fe3daaa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
# Wed, 11 May 2022 00:43:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed14c2edfc4c1e09a3dc29020e19fad2d064256d93ffbc664d1f2a35beca119`  
		Last Modified: Wed, 11 May 2022 00:45:48 GMT  
		Size: 6.9 MB (6935720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:bbce511525990d3eb217b0e66d1f437832ebdd28f0ee47ad7f21237424ed9a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:bf1326c676c31156a52c8c971b3b1f2b6b305b738fd7139053843a97205d76a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93858024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452e962280e8dbf51cf3c30175f89815f17c082b1f6c031533cb8f30553dbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Thu, 12 May 2022 19:19:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Thu, 12 May 2022 19:19:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 12 May 2022 19:19:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 12 May 2022 19:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 12 May 2022 19:19:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 May 2022 19:19:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 12 May 2022 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 19:19:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c649dd264dd33b4ef9c0d158dd48c75604a6b1f4a1ed4cda5419163771d1a72`  
		Last Modified: Thu, 12 May 2022 19:20:26 GMT  
		Size: 9.1 MB (9114016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6bf2632a9ad22f1eb0fac7ffa4d2a4b560db0b007313d6452b7e2e63a0784e`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be702489c9d0ff1211171ce9453d2ea77eea1127771988e5e3262e44e6dd6b5`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5f215a8dfbd4ad8c6f7e8a84379e8714a0b6a1cd25432b35170b614e32a70a`  
		Last Modified: Thu, 12 May 2022 19:20:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e18aeb402936db9a724855ca75c4dde8540fa1f71273aeadb2d3660800403a1e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86081746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ba2f3b7c338f7b9900c78c4605f7ce24d7083f09155221c24eeac44437b973`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 May 2022 00:39:33 GMT
ENV DOCKER_VERSION=20.10.15
# Fri, 06 May 2022 00:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 May 2022 00:42:54 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Wed, 11 May 2022 00:42:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 11 May 2022 00:42:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.0
# Wed, 11 May 2022 00:43:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64'; 			sha256='6296d17268c77a7159f57f04ed26dd2989f909c58cca4d44d1865f28bd27dd67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv6'; 			sha256='92b423e2c4d0ca0a979d7b6a4fb13707612f8fa19b900bc6cd1c2cf83f2780c5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-armv7'; 			sha256='d728dcbe5e20103e9b025efdbb6bfbca9ea9866851e669f7775fe3ebb7ab945c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-aarch64'; 			sha256='7efc61cc85fe712f14f04a6886d1481c96fe958be265f67482583b4b713b6a22'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-ppc64le'; 			sha256='e40af00a5f3ef87d31372f949134411b574042b8c055b2e5da12b92192405cb6'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-s390x'; 			sha256='c36e48910f095d07d582b69363fb3f902bb6fab9e2bd3d5ed82a67d1b2279a39'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 11 May 2022 00:43:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 May 2022 00:43:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 May 2022 00:43:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 May 2022 00:43:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 May 2022 00:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 00:43:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bace62412be99e37e41c6209417615e6e417cb0bdb8a0e509110a3b9b5af5b`  
		Last Modified: Fri, 06 May 2022 00:41:14 GMT  
		Size: 60.0 MB (59973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b8a1b3f8ca4629fce0550d02a91d6faf92e020a1cfa050c4e73fbeecffd0f`  
		Last Modified: Wed, 11 May 2022 00:44:37 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd73b57441486d29bba8adc690d019a81a58d55afb2144a0a0ee9f04c48b58b`  
		Last Modified: Wed, 11 May 2022 00:44:36 GMT  
		Size: 8.4 MB (8353176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1491e487ee15eff8d1484795137ca77e8c33cef424c8009f58efb98b55e498c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7428344a1d209df26c6007938ae720ca5314b7194aad26da9450b76c2fdfb3c`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf19d592fc22ab6b365349a62e52010658ab6d152e903ad319f7b2ac588820b7`  
		Last Modified: Wed, 11 May 2022 00:44:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:44251ae4b6e381ac726b35292cd0cedc2c9273e3b83991b56eca7290f59ee4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.707; amd64
	-	windows version 10.0.17763.2928; amd64

### `docker:windowsservercore` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:d63c51f65add3dd63c6d57455a72eda503f74a3d8b382c7b847942f75efdc12c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290667395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e6fc2818e4a6b2961fbf12c81c442c94666e05812a63248a527d57d0605c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:00 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:16:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9698df5d87653df3e05322abc936eba7b08b4ac1e1531d300326f852acb560d`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea315f146ff5d08a865f8afe9f6b3abbc0fbe3254d7c658afd18f2c6a6916c3`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c801fe2ce56a50e273ce72ad681cab5b3aff867063f17ed4a285d1d11f33e6`  
		Last Modified: Thu, 12 May 2022 19:19:40 GMT  
		Size: 52.5 MB (52523408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull docker@sha256:d91fe2d69d9526fb466c37afa1a7c5c14b3449caa82ead5ae8d88f081a98b8e7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556871108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963abf2508f0bb0b3f5da00f2a354a0c74d867eaabd99877b24cc991a6c99be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:17:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:53 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b919bb58ec3ed41b7e2e67e75497f0619d0f5ffa4ed0bf076d25d167186aed5`  
		Last Modified: Wed, 11 May 2022 01:19:58 GMT  
		Size: 486.0 KB (486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17963b29ee9a8eb140f806106b868925eef0ec9b9b9b7530399e44aa39644831`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794437e928236733907f6be03a38e33807049ff42b8df4f81f2585ce98a5cd`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fec92946e098247270b24628d39d2599af778a0f46841732c2d6180065fc43`  
		Last Modified: Thu, 12 May 2022 19:20:52 GMT  
		Size: 52.3 MB (52324957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:4298f49bbd424c400dc5d6e9f78f9710dc2abdde78924e61ec48bf4d10b649f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull docker@sha256:d91fe2d69d9526fb466c37afa1a7c5c14b3449caa82ead5ae8d88f081a98b8e7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556871108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963abf2508f0bb0b3f5da00f2a354a0c74d867eaabd99877b24cc991a6c99be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:17:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:53 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b919bb58ec3ed41b7e2e67e75497f0619d0f5ffa4ed0bf076d25d167186aed5`  
		Last Modified: Wed, 11 May 2022 01:19:58 GMT  
		Size: 486.0 KB (486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17963b29ee9a8eb140f806106b868925eef0ec9b9b9b7530399e44aa39644831`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794437e928236733907f6be03a38e33807049ff42b8df4f81f2585ce98a5cd`  
		Last Modified: Thu, 12 May 2022 19:19:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fec92946e098247270b24628d39d2599af778a0f46841732c2d6180065fc43`  
		Last Modified: Thu, 12 May 2022 19:20:52 GMT  
		Size: 52.3 MB (52324957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:025608dd7c48461a51e36543342256af22b1bc5933f311d3774503c2eaacd05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull docker@sha256:d63c51f65add3dd63c6d57455a72eda503f74a3d8b382c7b847942f75efdc12c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290667395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e6fc2818e4a6b2961fbf12c81c442c94666e05812a63248a527d57d0605c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 01:15:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 May 2022 19:16:00 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:16:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.16.zip
# Thu, 12 May 2022 19:16:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc0e7671236328b80eb96b578eb47d9bb8c85841986a699074c0abb105d7a6`  
		Last Modified: Wed, 11 May 2022 01:18:49 GMT  
		Size: 604.5 KB (604476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9698df5d87653df3e05322abc936eba7b08b4ac1e1531d300326f852acb560d`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea315f146ff5d08a865f8afe9f6b3abbc0fbe3254d7c658afd18f2c6a6916c3`  
		Last Modified: Thu, 12 May 2022 19:18:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c801fe2ce56a50e273ce72ad681cab5b3aff867063f17ed4a285d1d11f33e6`  
		Last Modified: Thu, 12 May 2022 19:19:40 GMT  
		Size: 52.5 MB (52523408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
