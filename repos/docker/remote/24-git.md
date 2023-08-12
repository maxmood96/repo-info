## `docker:24-git`

```console
$ docker pull docker@sha256:1f922e1dea940bda5fd79f59a16de998361e8a64c910f8e82559a6025935296d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-git` - linux; amd64

```console
$ docker pull docker@sha256:f39939d3e646ba3532025608ec6cd70f9225253d62df679db2377b88612f1915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123440487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5a427f5f5af49f13538ee019c8f3524a4147c1fbfe5b746b71e76354e1eec1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.3
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-x86_64'; 			sha256='f45e4cb687df8b48a57f656097ce7175fa8e8bef70be407b011e29ff663f475f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-armv6'; 			sha256='e2010f160f5077c6d4d777965d21147328dbfb29894e60a5fbbce716284fd3cf'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-armv7'; 			sha256='f62e5fb2e1908152c5f3e250faa2057c3d3351207eedd4c042ff540bba5f7575'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-aarch64'; 			sha256='9d6a6396b7604a390977ffff78379090f7c6910160bbd3b9669e2fcc635633c5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-ppc64le'; 			sha256='463d3d220da0fe49c40605a1fc9e4ed7414f47c0ac028c80c55d2e758e99d7ee'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-riscv64'; 			sha256='03b0ec338482f61593074b62ffab482ae67ecdc5d868eb72bb8fe3f8a7680c91'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-s390x'; 			sha256='3b24ddd85e859757801a8b9a7e53b96882fa5fd18cc12ee8750770f43b6afa14'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cddd6e4406982b82a6593306ca68f2264ab9596ad864331ad81f60609c0879`  
		Last Modified: Fri, 11 Aug 2023 18:50:35 GMT  
		Size: 2.0 MB (2014265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609329a09c8f3a09b827fc091fc43e913a91714a6f1c06b3d300cf4a176b7e6f`  
		Last Modified: Fri, 11 Aug 2023 18:50:36 GMT  
		Size: 16.4 MB (16390644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b2fbdc5adadc0919de3632414749dcb8aa94e790f9a0026a8df2e2f7c0723`  
		Last Modified: Fri, 11 Aug 2023 18:50:36 GMT  
		Size: 17.5 MB (17459266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4943246593c9ff296afb0ac7a5470ac23b9ffe8d31db5e1e1907ceea5616d3`  
		Last Modified: Fri, 11 Aug 2023 18:50:36 GMT  
		Size: 17.8 MB (17775005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9db0bb2866263a7b8b4c3bb309261faef5b693b93194a8c369f04c320fb956`  
		Last Modified: Fri, 11 Aug 2023 18:50:36 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a49a496a3422eb70428bc7e3a596d9b82d777efc63782c367dfbe74d14414ab`  
		Last Modified: Fri, 11 Aug 2023 18:50:37 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3e1e90b4863d51a12f2f198391cd5d7552962e4b6110ccc175a89cc64c0a61`  
		Last Modified: Fri, 11 Aug 2023 18:50:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150f5b2039cac6aea910879967003a6addbfa2d20207b63962dd27e76dd9f6f3`  
		Last Modified: Fri, 11 Aug 2023 19:50:44 GMT  
		Size: 7.1 MB (7080080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24c11514afe943e41f7465e47a6c324504f27747ed8e278767ee1f199f9ddcf`  
		Last Modified: Fri, 11 Aug 2023 19:50:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b523b76aab5ddf0b47c43b7c7978291b92b3fd386d049dff0f23371ba1d113`  
		Last Modified: Fri, 11 Aug 2023 19:50:48 GMT  
		Size: 54.4 MB (54377559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785edea07e4d086d6ca6cf795819bdc64a19404ae9404c503fef68424a846f21`  
		Last Modified: Fri, 11 Aug 2023 19:50:44 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2260d69ffa1ebc3e0603ce42b19c3cb73033d459186fe0554f8ede20a27d9c5`  
		Last Modified: Fri, 11 Aug 2023 19:50:44 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebec55ab336fe8331f8df7f4725c12d6495b5b71cf0f96cfa2c5d5e561c9fa7d`  
		Last Modified: Fri, 11 Aug 2023 20:50:54 GMT  
		Size: 4.9 MB (4935228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:44fae177437a6db7e1d2c5ac2c3eda522557a078fbeff80bd6c7aaa252c55d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.8 KB (814765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5f29f165827202e049303894b37d805469359563bf0a1ba36f31d684c82778`

```dockerfile
```

-	Layers:
	-	`sha256:ee1b8424bd7f4678ddeeaf1d9b5bfa6f4a07f2059a78ff275bd19e789b9d6d72`  
		Last Modified: Fri, 11 Aug 2023 20:50:53 GMT  
		Size: 801.8 KB (801836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa7a832a31aa93403a639fe0c6abf1a9044a22f0de0b3ea7471dcd9b2c04d570`  
		Last Modified: Fri, 11 Aug 2023 20:50:53 GMT  
		Size: 12.9 KB (12929 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3e45a34c487a9a092d1af58ae9e07a3e08d6f47c46490615bf960213e0ca0bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114830926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009ba2e6f1d9f2849105d5fe3d4126d66764f20e86e5bd9e776eee33ad8d0363`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.3
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-x86_64'; 			sha256='f45e4cb687df8b48a57f656097ce7175fa8e8bef70be407b011e29ff663f475f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-armv6'; 			sha256='e2010f160f5077c6d4d777965d21147328dbfb29894e60a5fbbce716284fd3cf'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-armv7'; 			sha256='f62e5fb2e1908152c5f3e250faa2057c3d3351207eedd4c042ff540bba5f7575'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-aarch64'; 			sha256='9d6a6396b7604a390977ffff78379090f7c6910160bbd3b9669e2fcc635633c5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-ppc64le'; 			sha256='463d3d220da0fe49c40605a1fc9e4ed7414f47c0ac028c80c55d2e758e99d7ee'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-riscv64'; 			sha256='03b0ec338482f61593074b62ffab482ae67ecdc5d868eb72bb8fe3f8a7680c91'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-s390x'; 			sha256='3b24ddd85e859757801a8b9a7e53b96882fa5fd18cc12ee8750770f43b6afa14'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6852f3ef0b5f9b77c7c21abf9035ed77c331514fd6aa1498370a5dbd3e2048b5`  
		Last Modified: Mon, 07 Aug 2023 22:18:57 GMT  
		Size: 2.0 MB (2024556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37278d121b4b21d7bddb02dabb1e78b7fc30c3f3a41e41d6f6967d040f3a1b54`  
		Last Modified: Mon, 07 Aug 2023 22:18:58 GMT  
		Size: 15.4 MB (15435452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c05b0ea06520d0d3c1e2b6753a684589ba3e17e586d4be8ad9ddfbb2d3b1d4c`  
		Last Modified: Mon, 07 Aug 2023 22:18:59 GMT  
		Size: 15.8 MB (15768051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841155fe5c5246b04de78ddfb5b3d9e86e638b598ca1a0994288ca878a5caf05`  
		Last Modified: Fri, 11 Aug 2023 19:43:26 GMT  
		Size: 16.2 MB (16233570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8fd905d97260664427a0d1237a908d90c4e0b0fb779b3f2cb2b968788fd35a`  
		Last Modified: Fri, 11 Aug 2023 19:43:24 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaebcfc8a783fcc13d4d726fb768712fb58105989aabc7a90cc62ac4f5c5d70`  
		Last Modified: Fri, 11 Aug 2023 19:43:24 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec782731361196526f7a8957ef4e2d269f2efc44c8b0a0db69f64ef22bc9a9a`  
		Last Modified: Fri, 11 Aug 2023 19:43:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020451d7f710b5af252779427cde32b2a2781a240984775374d0e81baa95e694`  
		Last Modified: Fri, 11 Aug 2023 19:51:09 GMT  
		Size: 7.3 MB (7291227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493c34e3a30de825e7c181bc495bb0da09a2a6ef61dd854249eabcf6395be178`  
		Last Modified: Fri, 11 Aug 2023 19:51:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f407d496aeeebb52651db2074c5fa6f4a0c1c2c24183e98c5a235cf445a66bd`  
		Last Modified: Fri, 11 Aug 2023 19:51:12 GMT  
		Size: 49.7 MB (49718885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b3658d625f5b575580c77db582b2c8237da0272a00d76c6d5047a6d514383`  
		Last Modified: Fri, 11 Aug 2023 19:51:09 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f0db26b16a336a77cdd90f317cf55f2332853b2dfea7b71a8ef1ca7854495`  
		Last Modified: Fri, 11 Aug 2023 19:51:10 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae03af2ff05a2dc56daa003ef7fbac309d1c1a2ae6204f951d89feb86b7dfa9`  
		Last Modified: Fri, 11 Aug 2023 21:05:01 GMT  
		Size: 5.0 MB (5021584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:815f8cf5c1665091259e323e80ccd31d15eac68ac62bd35495ffaf4b12c9494c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **812.8 KB (812813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23045f1838378230a07add00368664dd7eb8bf1931ddd50ee1faa2a589154cea`

```dockerfile
```

-	Layers:
	-	`sha256:a8113e22c65c5b503df1c1945874f8737dffeeba4a2376f3bf82f5b744b91815`  
		Last Modified: Fri, 11 Aug 2023 21:05:00 GMT  
		Size: 802.0 KB (802049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e7aaac72ae6944a7b57177c043b027f1bac158a96a4e2f7a7a8692a644427d`  
		Last Modified: Fri, 11 Aug 2023 21:05:00 GMT  
		Size: 10.8 KB (10764 bytes)  
		MIME: application/vnd.in-toto+json
