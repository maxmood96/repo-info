## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:5ef5498e925ca6cbe60e223dee4b398a71f758b1210ba469b0c1d2ab49a57156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:577df1d7311265910fd848abf536832a7a8f1d4e1814e55350543560b0ace1af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95455262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31317290e6df370d39dfeb98bc166241114ee80562a9770986f57581be3f74cb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 21:22:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Tue, 02 Jun 2020 21:22:38 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 31 Jul 2020 18:19:34 GMT
ENV DOCKER_CHANNEL=test
# Wed, 05 Aug 2020 09:39:11 GMT
ENV DOCKER_VERSION=19.03.13-beta2
# Wed, 05 Aug 2020 09:39:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 05 Aug 2020 09:39:17 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 05 Aug 2020 09:39:17 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 05 Aug 2020 09:39:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Aug 2020 09:39:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 05 Aug 2020 09:39:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Aug 2020 09:39:18 GMT
CMD ["sh"]
# Wed, 05 Aug 2020 09:39:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 05 Aug 2020 09:39:26 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 05 Aug 2020 09:39:26 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Wed, 05 Aug 2020 09:39:27 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 05 Aug 2020 09:39:27 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 05 Aug 2020 09:39:28 GMT
VOLUME [/var/lib/docker]
# Wed, 05 Aug 2020 09:39:28 GMT
EXPOSE 2375 2376
# Wed, 05 Aug 2020 09:39:28 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 05 Aug 2020 09:39:28 GMT
CMD []
# Wed, 05 Aug 2020 09:39:33 GMT
RUN apk add --no-cache iproute2
# Wed, 05 Aug 2020 09:39:34 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 05 Aug 2020 09:39:34 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 05 Aug 2020 09:39:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 05 Aug 2020 09:39:37 GMT
ENV ROOTLESSKIT_VERSION=0.10.0
# Wed, 05 Aug 2020 09:39:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 05 Aug 2020 09:39:48 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 05 Aug 2020 09:39:48 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 05 Aug 2020 09:39:49 GMT
USER rootless
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ad7478873d1d5c57089f038747520fe46aa4e913cc6cf29273b3722ec45e53`  
		Last Modified: Tue, 02 Jun 2020 21:23:34 GMT  
		Size: 2.0 MB (2040260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4684f6177b5d290b3aa892c1dc44088aa89f9ea08a68f6ed98262c032aa2caa4`  
		Last Modified: Tue, 02 Jun 2020 21:23:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7bc71302bb3ebb9b3da0925e5ab1f73f6cc11fb9c101b6027d47a5722a22a1`  
		Last Modified: Wed, 05 Aug 2020 09:40:41 GMT  
		Size: 61.2 MB (61188984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa883581c86da5877bd7c769cdf72741f06fb34eda145a1aed7f13115d18256`  
		Last Modified: Wed, 05 Aug 2020 09:40:29 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63137de011e0f62d4e549a758f4a17f246031b2db6cd234c6b8ebf8f7396a3e`  
		Last Modified: Wed, 05 Aug 2020 09:40:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963dfd0472c960bf328adc5d2f49540817dcf48d78e4d5b123dda32dd9ca5127`  
		Last Modified: Wed, 05 Aug 2020 09:40:29 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f4d368cf7c8374d6a272f33a5f6f21114ef9c5a3bda21997444d988eb8b190`  
		Last Modified: Wed, 05 Aug 2020 09:40:49 GMT  
		Size: 6.0 MB (5958764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88924d48d2dfed02b2c06ac23188876f2bc4a3957bd7a14dea4489367495b4b8`  
		Last Modified: Wed, 05 Aug 2020 09:40:48 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fccac7c8b32297091397a438129eac83b120a70dfc222cb44b639c486b6d68`  
		Last Modified: Wed, 05 Aug 2020 09:40:48 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d607daba1a35c6ffa9370321d88e3760d877b8794e2cea6272670c0f22577418`  
		Last Modified: Wed, 05 Aug 2020 09:40:48 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63983fb5758dc57e3b87a9a9beb500f4ff3745367b512f0678595e14cdb3c13a`  
		Last Modified: Wed, 05 Aug 2020 09:40:56 GMT  
		Size: 1.1 MB (1092686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b2755138e55ce505aef5774a90836992194efe5b2e634a5eb1db3b951e44cd`  
		Last Modified: Wed, 05 Aug 2020 09:40:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448c15ad7dc2fc7ee0746085b0b30e713929a6bebe55f8566a9b3c0880ec5e25`  
		Last Modified: Wed, 05 Aug 2020 09:40:55 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068a70a0f95434187a8601c1368ec469b75fd04d56f791a6b5a087482b1a2e5f`  
		Last Modified: Wed, 05 Aug 2020 09:40:58 GMT  
		Size: 9.1 MB (9109449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d373701278c4739c2aa50b0b0f93a506ed3077a8dcc671c00a3abe961a6d8a4`  
		Last Modified: Wed, 05 Aug 2020 09:40:57 GMT  
		Size: 13.3 MB (13259402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73ce1af5ebcd43fe2964c50314b228f8d7772a403f6c795e726a3a3f7b89184`  
		Last Modified: Wed, 05 Aug 2020 09:40:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
