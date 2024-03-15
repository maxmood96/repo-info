## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:9d9051ce6d1daf7ef81ec26284373b580eea3fc196076465f7a934c335d7e4fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ef10aa1e25605cb7afcfe75d6b36155d01adc9070389c9c969528efa13e877f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149136409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4e63a9a73ffafce46774ee23dd11f75be4836d033b369bdee837a4ea7c40fc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Mar 2024 21:18:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
CMD ["sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
VOLUME [/var/lib/docker]
# Thu, 07 Mar 2024 21:18:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 07 Mar 2024 21:18:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
CMD []
# Thu, 07 Mar 2024 21:18:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 07 Mar 2024 21:18:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf842b10bd29084c7b1d4ea339333dfbbcedda8e0061f5286540656fcd0c622`  
		Last Modified: Thu, 14 Mar 2024 17:49:09 GMT  
		Size: 2.0 MB (2018462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11b67e02f676c7dfd1f9990e830a72bd74b31ed5f7fe220936145ebd949559c`  
		Last Modified: Thu, 14 Mar 2024 17:49:09 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19906223ad476e3b60c28acbe61cc6d955293236f14ae2beb143c320356343cd`  
		Last Modified: Thu, 14 Mar 2024 17:49:10 GMT  
		Size: 16.9 MB (16921404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a024002a470447277fdbb9e42243277558ea56cf8d4e3960039065e7d3f8caa6`  
		Last Modified: Thu, 14 Mar 2024 17:49:10 GMT  
		Size: 18.0 MB (17982273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc50fed647043885df68fa8c68aa9aa245318ab660ef6d8fc5d2d9912fbcb37`  
		Last Modified: Thu, 14 Mar 2024 17:49:11 GMT  
		Size: 18.2 MB (18214531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2e82efe8f535a2191ba766fc3f85b7809faa4b04b39a9dd61a30481a17d836`  
		Last Modified: Thu, 14 Mar 2024 17:49:10 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24259fa21cdf3f784f07f620c6a53b3576443a19914b0a57dcc5b031bfe6b46e`  
		Last Modified: Thu, 14 Mar 2024 17:49:11 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7e3187d291fa1c8501eb8f7397e7d41176bc457cad3fe3f1889a4500450637`  
		Last Modified: Thu, 14 Mar 2024 17:49:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd1102f64f5db4bce94546687d19f1d0a64f1e0fe27b49cc6785152538e4fa`  
		Last Modified: Thu, 14 Mar 2024 18:49:15 GMT  
		Size: 12.2 MB (12156010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5384bc9959818d438b22a517564c88c60777ad0cf9c1d5df79d58f22db42426`  
		Last Modified: Thu, 14 Mar 2024 18:49:15 GMT  
		Size: 88.9 KB (88864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bdcd159f55536a6f329ef7706ef4d92ab457cefbe6bd640db13216585c3130`  
		Last Modified: Thu, 14 Mar 2024 18:49:15 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9332878e53fa5f694d45172c5906f9e46ec2827f87ca68b1259a9c8e0a6393`  
		Last Modified: Thu, 14 Mar 2024 18:49:16 GMT  
		Size: 56.4 MB (56368967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf9a92f3249f061ee6a6b27c68b4661b9b38175b1daec6054b2dd0e688eaf3`  
		Last Modified: Thu, 14 Mar 2024 18:49:16 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c166a377d301f696090dfb186658618e3baed04d4590b179abcc33ed54d3244b`  
		Last Modified: Thu, 14 Mar 2024 18:49:17 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8c6c832135a74d5e72b5ea76b4e8a339f52ade3bbba1556e4bd69203d5ee73`  
		Last Modified: Thu, 14 Mar 2024 19:48:14 GMT  
		Size: 981.3 KB (981299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89a73ae5fb909c16bdfc65932164a394c15eba282029535e49de5692219746`  
		Last Modified: Thu, 14 Mar 2024 19:48:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721f63a1a07529181502872afcbfe56997c87f4dd4dc0ab1fdc14e6cf29a67a0`  
		Last Modified: Thu, 14 Mar 2024 19:48:13 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4507543e5d080b503ff3a0dd77bf824b12aa4cbfb3fa9bf2d1d2dd65b8759e4`  
		Last Modified: Thu, 14 Mar 2024 19:48:15 GMT  
		Size: 21.0 MB (20985911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262dbb5d10d82bf4b2f6d3ec21c7c7804781f107b17d1cd60f7e6c32a33dbb37`  
		Last Modified: Thu, 14 Mar 2024 19:48:15 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:32c57e1044a495327a3b187407417433c9b0bf8b9aab440aff2d2c9e83651b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.0 KB (916962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef1eaacd8aa9b7d4ea96b0a7bdce0910a135851996a25953e6c98e5dede6de1`

```dockerfile
```

-	Layers:
	-	`sha256:cac28976686c982afc12a725d156dfd988181edbeb6901e4d4911a196e750f63`  
		Last Modified: Thu, 14 Mar 2024 19:48:14 GMT  
		Size: 884.0 KB (883967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e9488027485cf636ccf80590d6548df8054980dee328ed1ea618edd595cd5bc`  
		Last Modified: Thu, 14 Mar 2024 19:48:13 GMT  
		Size: 33.0 KB (32995 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8005989d09af04553c922f542013cde77d150d7956ad515a475d6ed8b91c2c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142906921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08f9344b7948bac4df89f2688f52501f0ac44af02e036c00af802b512e98a75`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-amd64'; 			sha256='ddd69ee2ca3dd61760e771dcd2f3453dc677dfeb42c9484cc2321b96bc1b7c57'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v6'; 			sha256='6aea498b2a168bcd13f919e85e0670c2e5a71abab8ecd6bfe52874d14680f617'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v7'; 			sha256='1566b6f3cf69d06ade467d9928e19f6a6682182fe3008bc9a0c83385d5637fa9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm64'; 			sha256='fa36eb4deab2fac6ddf5fdeddcf16999bc9d5fb1d632e0ba7e572b519df8a656'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-ppc64le'; 			sha256='aced23b7832c690703d0cb6339d4ccdbac9b45f0392b865b131aba9b572ae3c1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-riscv64'; 			sha256='c15e51986d59398552b3ecd50b4ca75779e42c878e34761df54616ac02165207'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-s390x'; 			sha256='c3578ab9814e4c2d0f917721b1dfd140b85e40602f6128745178a051cf4d0196'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Mar 2024 21:18:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
CMD ["sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
VOLUME [/var/lib/docker]
# Thu, 07 Mar 2024 21:18:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 07 Mar 2024 21:18:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
CMD []
# Thu, 07 Mar 2024 21:18:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 07 Mar 2024 21:18:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1445a503f72c73d6089a1119111ac23a281bc485cb856ca4679fe872c1a9ac8f`  
		Last Modified: Thu, 07 Mar 2024 18:50:58 GMT  
		Size: 2.0 MB (2019674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15768397550ab4bff548e50cb3f24c0a65a8e000b6e0f00a9930bd55c3889118`  
		Last Modified: Thu, 07 Mar 2024 18:50:57 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5ff57c43073dd456f690bcb3f53bf28b5b57645665a16d2ef1785555165df6`  
		Last Modified: Thu, 07 Mar 2024 23:51:19 GMT  
		Size: 15.9 MB (15936585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3754c60655d7a3f651b7b1cd9ab2ac1f6c0b7f664b2a1a09ee4be2a745e5782c`  
		Last Modified: Thu, 07 Mar 2024 23:51:20 GMT  
		Size: 16.3 MB (16349453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec1f585201afb2a1954af506937c8dfa7f7abe2d8b01e349613a0d64a3a2cc7`  
		Last Modified: Thu, 07 Mar 2024 23:51:20 GMT  
		Size: 16.6 MB (16643006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc54c7cd341012565f5076ea770bd73b4576c998f4f95d3a3433ac7c40d5bbd`  
		Last Modified: Thu, 07 Mar 2024 23:51:19 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e78b1e52249c5ebe1bcd126b0f097f406ffd079cbd4524565322f0c7851c960`  
		Last Modified: Thu, 07 Mar 2024 23:51:20 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bdfac3c1875e4e779413cd596214f5007025a7e4ff5c03800e8fde50c3d8e7`  
		Last Modified: Thu, 07 Mar 2024 23:51:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d86b45cb872b34953774c00d3311221a078cb428fa25c01b97fdd377ae9aa`  
		Last Modified: Fri, 08 Mar 2024 00:51:16 GMT  
		Size: 12.6 MB (12626836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a072988bf239d1699ab81a36bc808258ece10aa09e99e26b59e93549a4a1d49f`  
		Last Modified: Fri, 08 Mar 2024 00:51:16 GMT  
		Size: 98.4 KB (98380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e349905756b37ce70192105cfbc88a21eb915dd0896a9a474dd95e7a57c4183`  
		Last Modified: Fri, 08 Mar 2024 00:51:16 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e72e05c0bb69a3334235306d90dc3e43e3fe5c5ac0b029c798caf94f26586ef`  
		Last Modified: Fri, 08 Mar 2024 00:51:18 GMT  
		Size: 52.0 MB (52014210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a88d74d3c5a397033d8289646c94a2b38e4ed3870d4380640ba1f5cfa9abfbe`  
		Last Modified: Fri, 08 Mar 2024 00:51:17 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c4ae6e3e4d65b79f00bed3ebe554cad2e75dfb437f7ea6c09de91bbd341d72`  
		Last Modified: Fri, 08 Mar 2024 00:51:17 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e661498e8813c6906c4fe69fb8463c0b7e3fe0b30816120fbc9000cc3021ede9`  
		Last Modified: Fri, 08 Mar 2024 01:51:21 GMT  
		Size: 1.0 MB (1022486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8073658a9d2f5bfc2520592a2f1daa0921b6cee07f5e55ffd51165508c6c98`  
		Last Modified: Fri, 08 Mar 2024 01:51:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b49dabe7d1328736c076f3e1d3c11116b84b8accaa499094bf257e61970ced2`  
		Last Modified: Fri, 08 Mar 2024 01:51:21 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40fa4e2471140de8e1d5a298fd9b110882842aef4b8599d7e021970b78969e9`  
		Last Modified: Fri, 08 Mar 2024 01:51:22 GMT  
		Size: 22.8 MB (22838619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724dbf410575dd2cf6d7ff904b02f981eb90c191eb073259af23fa96e26446bd`  
		Last Modified: Fri, 08 Mar 2024 01:51:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:fb19e77806034d77896299c109465e5b8c6dab35c95e68d6c6dad99634d92dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.8 KB (917781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e24bb9fbc8d6addb1802622b3f5d19da126b1af7545f4f03d61b9c52dc9d29c`

```dockerfile
```

-	Layers:
	-	`sha256:8d6f2b6eeedeebeffc6616b6a9fb35f94737d85fbfc98405f95fbe489b327f09`  
		Last Modified: Fri, 08 Mar 2024 01:51:20 GMT  
		Size: 884.7 KB (884725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ebc7c064761e939d5561633a790aa4b89542345661c6e86250a3853435819a`  
		Last Modified: Fri, 08 Mar 2024 01:51:20 GMT  
		Size: 33.1 KB (33056 bytes)  
		MIME: application/vnd.in-toto+json
