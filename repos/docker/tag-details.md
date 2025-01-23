<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27-windowsservercore-ltsc2025`](#docker27-windowsservercore-ltsc2025)
-	[`docker:27.5`](#docker275)
-	[`docker:27.5-cli`](#docker275-cli)
-	[`docker:27.5-dind`](#docker275-dind)
-	[`docker:27.5-dind-rootless`](#docker275-dind-rootless)
-	[`docker:27.5-windowsservercore`](#docker275-windowsservercore)
-	[`docker:27.5-windowsservercore-1809`](#docker275-windowsservercore-1809)
-	[`docker:27.5-windowsservercore-ltsc2022`](#docker275-windowsservercore-ltsc2022)
-	[`docker:27.5-windowsservercore-ltsc2025`](#docker275-windowsservercore-ltsc2025)
-	[`docker:27.5.1`](#docker2751)
-	[`docker:27.5.1-alpine3.21`](#docker2751-alpine321)
-	[`docker:27.5.1-cli`](#docker2751-cli)
-	[`docker:27.5.1-cli-alpine3.21`](#docker2751-cli-alpine321)
-	[`docker:27.5.1-dind`](#docker2751-dind)
-	[`docker:27.5.1-dind-alpine3.21`](#docker2751-dind-alpine321)
-	[`docker:27.5.1-dind-rootless`](#docker2751-dind-rootless)
-	[`docker:27.5.1-windowsservercore`](#docker2751-windowsservercore)
-	[`docker:27.5.1-windowsservercore-1809`](#docker2751-windowsservercore-1809)
-	[`docker:27.5.1-windowsservercore-ltsc2022`](#docker2751-windowsservercore-ltsc2022)
-	[`docker:27.5.1-windowsservercore-ltsc2025`](#docker2751-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:27`

```console
$ docker pull docker@sha256:886e39f1390baaa74778366b228fc809ed8815a9235809ff8d2b038fdef0d09c
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

### `docker:27` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:5abfa3c0ff7d4add4395054751775d599a196874df408ea032b3892af0c2adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126344304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aef0003a941f9ed6335047bc2741dd2c754246e44b792596444ba505425924b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06b3967b4e642b2d6cb98ddda55dabc4993a3899194dfb50645801f28a2de4d`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.8 MB (18843467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e167d9a57b137b11ef1469f2536ba9c09315dd6e1858686fed99b317c474b`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.1 MB (18112380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746625955b5ebca8aee1d3e40c90c535484d1d6e5dcb2f3af36d50293db19d9b`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778bb8e57da23192256e4be8f68202f6916ae3d97cd410afd26a12c5157d2351`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f6729763aa7494d8f2673d92eaee47a0d1ff164b4022dad21403edbb87ac5`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143d81c732b89ee68c6854c26f60e4bd650052ccaa846e89b879dfd55f47d1e`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 7.0 MB (7041332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70697f77c3da37666380be4a8d5152894d73539601f5b1d05f7f6dfecbafdf40`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 89.1 KB (89095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462068e1d900fc5901c6341ff059c1d41259179a3231131a8a94fd3eaf64df4c`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f718a2a569cddb414e88527a1c82a5249ef00ed13d6d969d03fd6fe947be4b0`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877f61b5788c314f1cac1b07c0313c5527bc575bcd4d8b3272428ee623f3b274`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23f9c5dc2c1283e409e70ca0d2b4a332c5801dc25dc5843d1757ab106ed8c0`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:b1f9791b335c7b2bb6a757c468f291e693c2ccdf3877d6824d897eb61a4d54df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520c66be7ff520149482f170959560d0ba42369cac8764a5c7a7f77c5508bca8`

```dockerfile
```

-	Layers:
	-	`sha256:eeb9d59564585bc42c45673ed7070fabc5908a173de9834f878eda77da97e602`  
		Last Modified: Tue, 21 Jan 2025 21:07:25 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:f8f084af66dcc16af366577ae5c690b03d7cfac9e61cd0f96b8059a0fb45b973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124682037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540a5c12b45b516c76d8ea89c3597f0793e3798019bddf32d002d8f5ea5c33a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ac6636f9483ab54616b64903f8ba8d2cccee9440eb895c78d56ace8d3e4f96`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 6.4 MB (6367540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5348b12a83f89cbde850839c9f9cbbcb324c91ba1d7f5c1a142a6b282380fa8`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 85.2 KB (85240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eec605d713ebdd1bfff3c3503cc918cb50f85ece729d9770a8209d44099ddb7`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf469db7797818d99b9e99e927b899189f5993e54bb858b340b9eb4e3900a771`  
		Last Modified: Tue, 21 Jan 2025 21:07:31 GMT  
		Size: 54.0 MB (54047072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8360a16ab6657a3443418100cf468a24ee74c8c7e9eaa7582055fe8081c0140`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25fdd4000a14fc00def0dfdc4c82344e1c846243be32bb60c28b8d110b744d`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:3c7af3642f4779bc4148276b9902201860a53549bb11720b590ae5017cba85bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbf80603931802b71715d79b520e20f5ed851543f67792da506a4a5b901f599`

```dockerfile
```

-	Layers:
	-	`sha256:b8f59cb6e5ce03d8cfe1900ab25b26a4611e555e10cd4f04345b772825949593`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:1d07d717b4bce04c3446175b3d4bd6c7c16567fd8f061e992ad6c28f2d49054e
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

### `docker:27-cli` - linux; amd64

```console
$ docker pull docker@sha256:e1b7fa9b2d15b445084ecae08fb67d249c7748725a8731e0ef2d5fb5c54dba9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70091097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383208bbb6b0c1a0e235f583f3c8b7f80529e4ba7b91ff4952e988a75e57437b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4543eb003ef94a05439cb5446e2fe5d1a1318a77a5ecd0f7ce0f77bfde1f61`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 8.1 MB (8060130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b66b6f01517380357ef07c7409f00407748f8e744c0eb5ed5efe498c2e5bb`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df855c4e32dd197ba449da2be8641932cbc5879636990104ef951c56eaf1b82`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 18.8 MB (18848905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b6742bd2d5a6242c709b92cf93f22139461e1ff302a6f601fd1cabf1af7580`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 20.2 MB (20234555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af9ba02f40bd06616eacbd5670ba2485bd87a92b4c972cf5bf1120ff27aa1b`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1193bea83fc8c129bcfd73718e8e96feb49527eb743470a8f08e0ccc8a9ec2b3`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae3e6f1bf5bb5465e3db71bb733f3cacc996333fbee14a57bef4eb56ce912`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046ca50013a72571a456c1a5437df9fe09fe9be0f35107d9a6a20518449da42`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:13bf5de648cb5dcec33c01c66cc8cc55752b09fd237dce16215654738d142689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07d5481f565c713cf6c1f3c29a788fe00c89b8ec831200bf121baa5ffc40bde`

```dockerfile
```

-	Layers:
	-	`sha256:d631712da516c7c8bd3f89066d3f8f96905f5d19845d63d390476765e524e735`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:67daf59d1ebdf055fc86f315690f99720fe2e76c422f47c3f15cbd59798a7781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65161798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8395e26813af8fba5ddfef47bb16e82d996373cb799de4b15c2204ffe8725ca3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed4e5240126a237686beb0364732ea8fb90b8222bb79ece3b01bc65f11255f8`  
		Last Modified: Thu, 23 Jan 2025 01:08:51 GMT  
		Size: 16.9 MB (16866758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc64aa21acc52ff9715cac0a1c9950afe80cf8a4ea1a68baec921a635cb58a9b`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.8 MB (18843713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac9ccf0752d89cd64424f0e836d6a53bcf608d2ade5c57f9e268310298d7c8`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.1 MB (18112376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee11d500ae760463d5de6d7e1832499db3e5428c8aa304592b37e53e49d17d5`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e7eeefb54f6e84b1a476d04890600e732afcfbb674962f1d0af1f84c3b20f8`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089baa8d0b7e233427ebf7a6ec651326f37ce677522489b2445fa3a8ddf54820`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5b461226ce2d9537eecdcd27c8103b253c6453c497ac8b2c67e62f43b19e4651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769dd3e9bae0849e1af06e8b2ed0bb521e30956eb80ad18e01d1fbd4072b8976`

```dockerfile
```

-	Layers:
	-	`sha256:0a463fb4d15db5c2a23b7371f79cc40b855f69ffe02bd964e646b412a881d150`  
		Last Modified: Thu, 23 Jan 2025 01:28:08 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:0091be5184eae4250fc1cb11a01fe5ea066d1b7a846c67a6d23e817d010260a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64176388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7773e8edbbc039cd622aa68e12968928793e28dc0fd375c732981a7e42162a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 21 Jan 2025 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d503a1f6ea902951cfe37f5418137ffcd9c643beb7df1964bd2e45c83ef6f07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d161766fb8c4a9cb705ff2b79fe8c2fc98c84779426e81316089633605422d`

```dockerfile
```

-	Layers:
	-	`sha256:79bd3d5210a7b1bf892a818f3142ff8a95fb47d2845f0667fb2b28d4ed3d1b6b`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6f1a1a24027716e44d9b7a08b7252bf33c60403dd92c77bf863d625a15bf302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65972403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581c2c02c852d766afb66b604dbd45f44c1bdd42eb5cb2c127663c9e3954b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d47d71a04452163577e439ccf4d91457ac4ab2f7fa68cc32517b973eae562185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bbc8c969ef865647e5cf02166f155e554bf917314e431725c57c35399e34f1`

```dockerfile
```

-	Layers:
	-	`sha256:15793555fc85eacaeec2b45b37d648b58e45b2ba5fcb0e42884c619c7eb12885`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:886e39f1390baaa74778366b228fc809ed8815a9235809ff8d2b038fdef0d09c
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

### `docker:27-dind` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:5abfa3c0ff7d4add4395054751775d599a196874df408ea032b3892af0c2adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126344304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aef0003a941f9ed6335047bc2741dd2c754246e44b792596444ba505425924b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06b3967b4e642b2d6cb98ddda55dabc4993a3899194dfb50645801f28a2de4d`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.8 MB (18843467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e167d9a57b137b11ef1469f2536ba9c09315dd6e1858686fed99b317c474b`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.1 MB (18112380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746625955b5ebca8aee1d3e40c90c535484d1d6e5dcb2f3af36d50293db19d9b`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778bb8e57da23192256e4be8f68202f6916ae3d97cd410afd26a12c5157d2351`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f6729763aa7494d8f2673d92eaee47a0d1ff164b4022dad21403edbb87ac5`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143d81c732b89ee68c6854c26f60e4bd650052ccaa846e89b879dfd55f47d1e`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 7.0 MB (7041332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70697f77c3da37666380be4a8d5152894d73539601f5b1d05f7f6dfecbafdf40`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 89.1 KB (89095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462068e1d900fc5901c6341ff059c1d41259179a3231131a8a94fd3eaf64df4c`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f718a2a569cddb414e88527a1c82a5249ef00ed13d6d969d03fd6fe947be4b0`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877f61b5788c314f1cac1b07c0313c5527bc575bcd4d8b3272428ee623f3b274`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23f9c5dc2c1283e409e70ca0d2b4a332c5801dc25dc5843d1757ab106ed8c0`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b1f9791b335c7b2bb6a757c468f291e693c2ccdf3877d6824d897eb61a4d54df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520c66be7ff520149482f170959560d0ba42369cac8764a5c7a7f77c5508bca8`

```dockerfile
```

-	Layers:
	-	`sha256:eeb9d59564585bc42c45673ed7070fabc5908a173de9834f878eda77da97e602`  
		Last Modified: Tue, 21 Jan 2025 21:07:25 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f8f084af66dcc16af366577ae5c690b03d7cfac9e61cd0f96b8059a0fb45b973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124682037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540a5c12b45b516c76d8ea89c3597f0793e3798019bddf32d002d8f5ea5c33a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ac6636f9483ab54616b64903f8ba8d2cccee9440eb895c78d56ace8d3e4f96`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 6.4 MB (6367540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5348b12a83f89cbde850839c9f9cbbcb324c91ba1d7f5c1a142a6b282380fa8`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 85.2 KB (85240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eec605d713ebdd1bfff3c3503cc918cb50f85ece729d9770a8209d44099ddb7`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf469db7797818d99b9e99e927b899189f5993e54bb858b340b9eb4e3900a771`  
		Last Modified: Tue, 21 Jan 2025 21:07:31 GMT  
		Size: 54.0 MB (54047072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8360a16ab6657a3443418100cf468a24ee74c8c7e9eaa7582055fe8081c0140`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25fdd4000a14fc00def0dfdc4c82344e1c846243be32bb60c28b8d110b744d`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3c7af3642f4779bc4148276b9902201860a53549bb11720b590ae5017cba85bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbf80603931802b71715d79b520e20f5ed851543f67792da506a4a5b901f599`

```dockerfile
```

-	Layers:
	-	`sha256:b8f59cb6e5ce03d8cfe1900ab25b26a4611e555e10cd4f04345b772825949593`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:5894f4cff8223ed0e1cfcab0d451849166a27cf9bd88bf7d83c53bb0bdad775c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ebd049ca6195b27ec4d34483b4e38e88515c9bfeb884537a44f08a2fe05d5f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157613241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6353ec2f724bd821b6dd3bcad22c0c0213128ff2c9331f636c702b4dd81afe40`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2030ef23a285bdccc40ad0b8ce9efd335fa61d75066bd807c3c82aeac0f5f88`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 986.6 KB (986595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061b18067d315bf70f729ee154e161b68bbe16810de94c1d627a4c781f721c3f`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2867fc390a21dec4f2ebdbb9300bf3927b4896771538473397c8af0916a37254`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0483bcb96635778b03e6a5ff71821e008f3b7ce018ce583db4445025063d703`  
		Last Modified: Wed, 22 Jan 2025 21:10:25 GMT  
		Size: 21.3 MB (21319725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b23e1fe72a9f72a4cf162d1c5061014d374dacd1d4100f237be5d25a322a`  
		Last Modified: Wed, 22 Jan 2025 21:10:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f55d62345aa0a7d862bbd0b6823a21e050a79f4e9d5e6d5d65e4c49e4574c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e295f522e42b2f55e6fd395f80567bc863c970e296904d50e89e25eb29e3000f`

```dockerfile
```

-	Layers:
	-	`sha256:35de99a4851778ee6250f309e86dae0f1fb8984bdcbc582760697bcf74974b11`  
		Last Modified: Wed, 22 Jan 2025 21:10:23 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:833312f4f1a9ef7036f2eb35dc25b09b976770a5326fe1ae0c2eff1694329dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151181458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa2e4d37c474367c7177f81b11d61750fde80a813648fb40a7fba203a66a14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b727576946f5ef0ee11736742c4ff0470a45828e4ce130d8e5158a71cdc4515a`  
		Last Modified: Tue, 21 Jan 2025 20:44:26 GMT  
		Size: 8.1 MB (8074424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2959c0b73dae5e70c97573b56c908480cc4794318911d7610b30a7d08add5e67`  
		Last Modified: Tue, 21 Jan 2025 20:44:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9d6033bb3f386bb327c2a9dea343cefc26aeb5b2e417d7c983657640216e63`  
		Last Modified: Tue, 21 Jan 2025 20:44:26 GMT  
		Size: 17.8 MB (17795758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71047f9f9e392480cc32ed9ac2fc6ed8585cce97a79dc96a0930c972f75ca660`  
		Last Modified: Tue, 21 Jan 2025 20:44:26 GMT  
		Size: 18.5 MB (18458817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b817e8d2b390c439babdc0043d6cf2b5759fb141bd00c9afda6079131e738`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c318310707fb7d70580473eefb15f5bafd42ed152cffed011782dea9d4f3c0`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07193a6ec91b4162516067c96e1ef0e311d7040662f575641cfd216ba9fb1b6f`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508661da5f6d786932535a6222a1c9ab8241662fa84c4aa1fe7f0e696bb814dd`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aeabb3b339362e97bb858dde3992bea728a71c3383d745f93e427151713b6c7`  
		Last Modified: Tue, 21 Jan 2025 21:07:33 GMT  
		Size: 7.0 MB (6981856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c10601a92c5b122e04503bcb1e83c4f3f82a117bc4e728e37b9e391f59211f9`  
		Last Modified: Tue, 21 Jan 2025 21:07:32 GMT  
		Size: 97.8 KB (97787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f958e3424c382e9adc12d77fcbbd8874e403b5b88b7c90902a67d15c890e59`  
		Last Modified: Tue, 21 Jan 2025 21:07:32 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e6227060ad9047fcb92528e802e2346e3dd60dc992edf63a3d4d013ead61e6`  
		Last Modified: Tue, 21 Jan 2025 21:07:34 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4f193ab21aed60d8c9fec5613d685cb40335600aa233556a06505e0ef5318`  
		Last Modified: Tue, 21 Jan 2025 21:07:33 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759900d45cbe5d399f81c58532e5522310c16f03afe794a0bf3a50b5fd054c77`  
		Last Modified: Tue, 21 Jan 2025 21:07:33 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cb4aa93ab603e4d4d33d7d2d3f82369c3e359048c6fdb08875b0afb9cc03dc`  
		Last Modified: Tue, 21 Jan 2025 22:26:04 GMT  
		Size: 1.0 MB (1014210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e90b89b9be7fcda0f00b817afa36b2749564c4e99751d5c7058e402b66bf48b`  
		Last Modified: Tue, 21 Jan 2025 22:26:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0513e4ce7390c12c9bc93c6159f762dfe4f7e3c360539df0d7cf96de1707f108`  
		Last Modified: Tue, 21 Jan 2025 22:26:06 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e28a5e173d0d71747307dbbe2bb458536d5a9afe7d6ec4763579c7263115aa`  
		Last Modified: Tue, 21 Jan 2025 22:26:08 GMT  
		Size: 23.2 MB (23155149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeb43a8221adfbb3e388e9580b0ba5a29a4333f64965bc4faaa84858ecf1cce`  
		Last Modified: Tue, 21 Jan 2025 22:26:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:caead8335948168299f106e6d8abf4c8bb107a57c7bd57a767a7632ff3de974b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d57ab7f48c566a66a83a0468613379b200f3ca872f028c4dca41036e58ac2b3`

```dockerfile
```

-	Layers:
	-	`sha256:2267704e3c4977b5238c0b47cc65ef3aa58a5fc69b1b7e7c49e70fede78cb64e`  
		Last Modified: Tue, 21 Jan 2025 22:26:06 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:b6f8b0d57df4a2696419a5762e577d335b8045344e3955e8f4dbe161e18af19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Thu, 23 Jan 2025 01:33:30 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:5c1a568071d5c38211f0f2ab29165658baa270218a50280ea14a48e551fdb8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323144969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7fa5f72ee91f71047e0cae9811ca6f53ba1a60cdb312db0a9d0345798a4187`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 01:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:28:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:28:53 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:28:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:29:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:29:14 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:29:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed09903d475f8bbfa96b9ead8ead4f2a39d0f719b474586e24a4a58b9470345e`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52dc955ea9bebcaa9ed296818141638ea1aacbed9fdba231dc54b2980b65a5c`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 361.5 KB (361541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a2af8cdcfc4a587bf767381b48afc6c8a51de1f15d8bc0b58ab40283a5f4b`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03fc4d8fe06a92147d6a07ecb5da93751eb8bba0ddcf071c2c3cae0a21b87e3`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb589666dc5302c33e2bd3103275dce7cc6d806c1f7941c8b7d21cfb86111fdc`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 19.1 MB (19134262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a47ad75b95b47fedf86cc1b64b2ee05f4d918b17abd048778f49815048d7510`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38a2eb0cc0556e4da418dfa0ee2cdc500a1f6939268795cfc7257456825f41`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f4b5f8bb28da0ae8bbf98a59430a7a7bc9c34fd58f375b55d628b8b87ab0b7`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c4b941c28c51cd43369ba6156390bdf5fb913aeb0f27ac099875fe7524cae4`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 21.1 MB (21112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d65a4d2b1bb37dc218ab758d1ceee791d50caec34bb6831847c4a8160c67a`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e41bf06ac3da01d5d8fad12e4accd484fedf4eba4a806a136587de0f9b1cda`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ae2d6a0e330b4f2d8f8b93d611370649ad1f85767b559b921a5c1ee27b5bd`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8b1dd36f2eb10913aef8028fb60fb8cd6ef11f7e112ee8ffbbe965253d530`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 20.1 MB (20140156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:38bc4d48f3168306d2d648e0af9406d27bb41a6537d46185c81cefb8ebef842d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183020077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3b61b7f9129666ce834144f71d29ff871f27da200bb6cf5e5f7c0aef7c6ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 01:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:35:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:35:13 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:35:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:35:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:35:29 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:35:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:35:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e1f7a6ddd0af874949fad5fb2b18dc713d63a1972a77488e76118dd264f9d6`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33a1f96da749ae14a963290552db28406e792510359e069b46c86dcf63dc44`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 339.2 KB (339235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72e1a49e563e9bd93904b22396c2cd2f02b470a1bde810aa4003c0ef0ab56`  
		Last Modified: Thu, 23 Jan 2025 01:36:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a932c4224a159c091a14b8d1fe2b1c82bd3a605f046e5770a30f20464d41`  
		Last Modified: Thu, 23 Jan 2025 01:35:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60ccc3c7b375c18d01ab1d49ab7bbe737fc195d6d8e69b61742a296795eb775`  
		Last Modified: Thu, 23 Jan 2025 01:36:01 GMT  
		Size: 19.2 MB (19162080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbc1c67f17e5b2e533cc4d4cbf4892631ec102977971247237ed7b91d36994`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4841f280b69012015b175aa6b6f87bc6d793a6e8d36f300ad59f649531a6d1`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d47b4005db434e43608202c5acadac1e39ac41c7da57dc0ed3db8b450198b6f`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ce7b9a878c3aff2e2a97b385f7c75f6043234bb92a724f5f7c060be0032be1`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 21.1 MB (21130564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd9a849c2c7eefd648403d5cd4e04a259de2927c100bc629bbbb132b5f821c3`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5505d56ad65828edc87e543f61694fe4bc77d3be290c27ecf695f8625ba2c415`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce02b8200d83f1b73eeee2e5797bdb4fe5b87497dea1b31c3a655e45cd8d011c`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042952d001e4adcdab5611fa007695ef67a2707230a2be2278cd1fc6cea222a4`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 20.2 MB (20163992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:383bafe0d882dfaee478abe15a862e5a2cbd50cef39a1ca7bfa511fdff4053cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:38bc4d48f3168306d2d648e0af9406d27bb41a6537d46185c81cefb8ebef842d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183020077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3b61b7f9129666ce834144f71d29ff871f27da200bb6cf5e5f7c0aef7c6ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 01:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:35:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:35:13 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:35:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:35:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:35:29 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:35:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:35:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e1f7a6ddd0af874949fad5fb2b18dc713d63a1972a77488e76118dd264f9d6`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33a1f96da749ae14a963290552db28406e792510359e069b46c86dcf63dc44`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 339.2 KB (339235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72e1a49e563e9bd93904b22396c2cd2f02b470a1bde810aa4003c0ef0ab56`  
		Last Modified: Thu, 23 Jan 2025 01:36:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a932c4224a159c091a14b8d1fe2b1c82bd3a605f046e5770a30f20464d41`  
		Last Modified: Thu, 23 Jan 2025 01:35:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60ccc3c7b375c18d01ab1d49ab7bbe737fc195d6d8e69b61742a296795eb775`  
		Last Modified: Thu, 23 Jan 2025 01:36:01 GMT  
		Size: 19.2 MB (19162080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbc1c67f17e5b2e533cc4d4cbf4892631ec102977971247237ed7b91d36994`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4841f280b69012015b175aa6b6f87bc6d793a6e8d36f300ad59f649531a6d1`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d47b4005db434e43608202c5acadac1e39ac41c7da57dc0ed3db8b450198b6f`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ce7b9a878c3aff2e2a97b385f7c75f6043234bb92a724f5f7c060be0032be1`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 21.1 MB (21130564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd9a849c2c7eefd648403d5cd4e04a259de2927c100bc629bbbb132b5f821c3`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5505d56ad65828edc87e543f61694fe4bc77d3be290c27ecf695f8625ba2c415`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce02b8200d83f1b73eeee2e5797bdb4fe5b87497dea1b31c3a655e45cd8d011c`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042952d001e4adcdab5611fa007695ef67a2707230a2be2278cd1fc6cea222a4`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 20.2 MB (20163992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c37cf3b88ac15878732da1a35ced92a3889e31d4512d22dac218f03dc9cedb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:5c1a568071d5c38211f0f2ab29165658baa270218a50280ea14a48e551fdb8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323144969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7fa5f72ee91f71047e0cae9811ca6f53ba1a60cdb312db0a9d0345798a4187`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 01:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:28:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:28:53 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:28:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:29:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:29:14 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:29:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed09903d475f8bbfa96b9ead8ead4f2a39d0f719b474586e24a4a58b9470345e`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52dc955ea9bebcaa9ed296818141638ea1aacbed9fdba231dc54b2980b65a5c`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 361.5 KB (361541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a2af8cdcfc4a587bf767381b48afc6c8a51de1f15d8bc0b58ab40283a5f4b`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03fc4d8fe06a92147d6a07ecb5da93751eb8bba0ddcf071c2c3cae0a21b87e3`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb589666dc5302c33e2bd3103275dce7cc6d806c1f7941c8b7d21cfb86111fdc`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 19.1 MB (19134262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a47ad75b95b47fedf86cc1b64b2ee05f4d918b17abd048778f49815048d7510`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38a2eb0cc0556e4da418dfa0ee2cdc500a1f6939268795cfc7257456825f41`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f4b5f8bb28da0ae8bbf98a59430a7a7bc9c34fd58f375b55d628b8b87ab0b7`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c4b941c28c51cd43369ba6156390bdf5fb913aeb0f27ac099875fe7524cae4`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 21.1 MB (21112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d65a4d2b1bb37dc218ab758d1ceee791d50caec34bb6831847c4a8160c67a`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e41bf06ac3da01d5d8fad12e4accd484fedf4eba4a806a136587de0f9b1cda`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ae2d6a0e330b4f2d8f8b93d611370649ad1f85767b559b921a5c1ee27b5bd`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8b1dd36f2eb10913aef8028fb60fb8cd6ef11f7e112ee8ffbbe965253d530`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 20.1 MB (20140156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c68bdfb265f8b44bdcdbd856c52b597a0adc9e70d38d1073c2dcbeb23e26818e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:27-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Thu, 23 Jan 2025 01:33:30 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5`

```console
$ docker pull docker@sha256:886e39f1390baaa74778366b228fc809ed8815a9235809ff8d2b038fdef0d09c
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

### `docker:27.5` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5` - linux; arm variant v6

```console
$ docker pull docker@sha256:5abfa3c0ff7d4add4395054751775d599a196874df408ea032b3892af0c2adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126344304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aef0003a941f9ed6335047bc2741dd2c754246e44b792596444ba505425924b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06b3967b4e642b2d6cb98ddda55dabc4993a3899194dfb50645801f28a2de4d`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.8 MB (18843467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e167d9a57b137b11ef1469f2536ba9c09315dd6e1858686fed99b317c474b`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.1 MB (18112380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746625955b5ebca8aee1d3e40c90c535484d1d6e5dcb2f3af36d50293db19d9b`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778bb8e57da23192256e4be8f68202f6916ae3d97cd410afd26a12c5157d2351`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f6729763aa7494d8f2673d92eaee47a0d1ff164b4022dad21403edbb87ac5`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143d81c732b89ee68c6854c26f60e4bd650052ccaa846e89b879dfd55f47d1e`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 7.0 MB (7041332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70697f77c3da37666380be4a8d5152894d73539601f5b1d05f7f6dfecbafdf40`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 89.1 KB (89095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462068e1d900fc5901c6341ff059c1d41259179a3231131a8a94fd3eaf64df4c`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f718a2a569cddb414e88527a1c82a5249ef00ed13d6d969d03fd6fe947be4b0`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877f61b5788c314f1cac1b07c0313c5527bc575bcd4d8b3272428ee623f3b274`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23f9c5dc2c1283e409e70ca0d2b4a332c5801dc25dc5843d1757ab106ed8c0`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:b1f9791b335c7b2bb6a757c468f291e693c2ccdf3877d6824d897eb61a4d54df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520c66be7ff520149482f170959560d0ba42369cac8764a5c7a7f77c5508bca8`

```dockerfile
```

-	Layers:
	-	`sha256:eeb9d59564585bc42c45673ed7070fabc5908a173de9834f878eda77da97e602`  
		Last Modified: Tue, 21 Jan 2025 21:07:25 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5` - linux; arm variant v7

```console
$ docker pull docker@sha256:f8f084af66dcc16af366577ae5c690b03d7cfac9e61cd0f96b8059a0fb45b973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124682037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540a5c12b45b516c76d8ea89c3597f0793e3798019bddf32d002d8f5ea5c33a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ac6636f9483ab54616b64903f8ba8d2cccee9440eb895c78d56ace8d3e4f96`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 6.4 MB (6367540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5348b12a83f89cbde850839c9f9cbbcb324c91ba1d7f5c1a142a6b282380fa8`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 85.2 KB (85240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eec605d713ebdd1bfff3c3503cc918cb50f85ece729d9770a8209d44099ddb7`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf469db7797818d99b9e99e927b899189f5993e54bb858b340b9eb4e3900a771`  
		Last Modified: Tue, 21 Jan 2025 21:07:31 GMT  
		Size: 54.0 MB (54047072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8360a16ab6657a3443418100cf468a24ee74c8c7e9eaa7582055fe8081c0140`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25fdd4000a14fc00def0dfdc4c82344e1c846243be32bb60c28b8d110b744d`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:3c7af3642f4779bc4148276b9902201860a53549bb11720b590ae5017cba85bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbf80603931802b71715d79b520e20f5ed851543f67792da506a4a5b901f599`

```dockerfile
```

-	Layers:
	-	`sha256:b8f59cb6e5ce03d8cfe1900ab25b26a4611e555e10cd4f04345b772825949593`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-cli`

```console
$ docker pull docker@sha256:1d07d717b4bce04c3446175b3d4bd6c7c16567fd8f061e992ad6c28f2d49054e
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

### `docker:27.5-cli` - linux; amd64

```console
$ docker pull docker@sha256:e1b7fa9b2d15b445084ecae08fb67d249c7748725a8731e0ef2d5fb5c54dba9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70091097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383208bbb6b0c1a0e235f583f3c8b7f80529e4ba7b91ff4952e988a75e57437b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4543eb003ef94a05439cb5446e2fe5d1a1318a77a5ecd0f7ce0f77bfde1f61`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 8.1 MB (8060130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b66b6f01517380357ef07c7409f00407748f8e744c0eb5ed5efe498c2e5bb`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df855c4e32dd197ba449da2be8641932cbc5879636990104ef951c56eaf1b82`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 18.8 MB (18848905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b6742bd2d5a6242c709b92cf93f22139461e1ff302a6f601fd1cabf1af7580`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 20.2 MB (20234555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af9ba02f40bd06616eacbd5670ba2485bd87a92b4c972cf5bf1120ff27aa1b`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1193bea83fc8c129bcfd73718e8e96feb49527eb743470a8f08e0ccc8a9ec2b3`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae3e6f1bf5bb5465e3db71bb733f3cacc996333fbee14a57bef4eb56ce912`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046ca50013a72571a456c1a5437df9fe09fe9be0f35107d9a6a20518449da42`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:13bf5de648cb5dcec33c01c66cc8cc55752b09fd237dce16215654738d142689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07d5481f565c713cf6c1f3c29a788fe00c89b8ec831200bf121baa5ffc40bde`

```dockerfile
```

-	Layers:
	-	`sha256:d631712da516c7c8bd3f89066d3f8f96905f5d19845d63d390476765e524e735`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:67daf59d1ebdf055fc86f315690f99720fe2e76c422f47c3f15cbd59798a7781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65161798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8395e26813af8fba5ddfef47bb16e82d996373cb799de4b15c2204ffe8725ca3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed4e5240126a237686beb0364732ea8fb90b8222bb79ece3b01bc65f11255f8`  
		Last Modified: Thu, 23 Jan 2025 01:08:51 GMT  
		Size: 16.9 MB (16866758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc64aa21acc52ff9715cac0a1c9950afe80cf8a4ea1a68baec921a635cb58a9b`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.8 MB (18843713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac9ccf0752d89cd64424f0e836d6a53bcf608d2ade5c57f9e268310298d7c8`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.1 MB (18112376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee11d500ae760463d5de6d7e1832499db3e5428c8aa304592b37e53e49d17d5`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e7eeefb54f6e84b1a476d04890600e732afcfbb674962f1d0af1f84c3b20f8`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089baa8d0b7e233427ebf7a6ec651326f37ce677522489b2445fa3a8ddf54820`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5b461226ce2d9537eecdcd27c8103b253c6453c497ac8b2c67e62f43b19e4651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769dd3e9bae0849e1af06e8b2ed0bb521e30956eb80ad18e01d1fbd4072b8976`

```dockerfile
```

-	Layers:
	-	`sha256:0a463fb4d15db5c2a23b7371f79cc40b855f69ffe02bd964e646b412a881d150`  
		Last Modified: Thu, 23 Jan 2025 01:28:08 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:0091be5184eae4250fc1cb11a01fe5ea066d1b7a846c67a6d23e817d010260a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64176388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7773e8edbbc039cd622aa68e12968928793e28dc0fd375c732981a7e42162a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 21 Jan 2025 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d503a1f6ea902951cfe37f5418137ffcd9c643beb7df1964bd2e45c83ef6f07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d161766fb8c4a9cb705ff2b79fe8c2fc98c84779426e81316089633605422d`

```dockerfile
```

-	Layers:
	-	`sha256:79bd3d5210a7b1bf892a818f3142ff8a95fb47d2845f0667fb2b28d4ed3d1b6b`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6f1a1a24027716e44d9b7a08b7252bf33c60403dd92c77bf863d625a15bf302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65972403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581c2c02c852d766afb66b604dbd45f44c1bdd42eb5cb2c127663c9e3954b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d47d71a04452163577e439ccf4d91457ac4ab2f7fa68cc32517b973eae562185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bbc8c969ef865647e5cf02166f155e554bf917314e431725c57c35399e34f1`

```dockerfile
```

-	Layers:
	-	`sha256:15793555fc85eacaeec2b45b37d648b58e45b2ba5fcb0e42884c619c7eb12885`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-dind`

```console
$ docker pull docker@sha256:886e39f1390baaa74778366b228fc809ed8815a9235809ff8d2b038fdef0d09c
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

### `docker:27.5-dind` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:5abfa3c0ff7d4add4395054751775d599a196874df408ea032b3892af0c2adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126344304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aef0003a941f9ed6335047bc2741dd2c754246e44b792596444ba505425924b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06b3967b4e642b2d6cb98ddda55dabc4993a3899194dfb50645801f28a2de4d`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.8 MB (18843467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e167d9a57b137b11ef1469f2536ba9c09315dd6e1858686fed99b317c474b`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.1 MB (18112380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746625955b5ebca8aee1d3e40c90c535484d1d6e5dcb2f3af36d50293db19d9b`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778bb8e57da23192256e4be8f68202f6916ae3d97cd410afd26a12c5157d2351`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f6729763aa7494d8f2673d92eaee47a0d1ff164b4022dad21403edbb87ac5`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143d81c732b89ee68c6854c26f60e4bd650052ccaa846e89b879dfd55f47d1e`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 7.0 MB (7041332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70697f77c3da37666380be4a8d5152894d73539601f5b1d05f7f6dfecbafdf40`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 89.1 KB (89095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462068e1d900fc5901c6341ff059c1d41259179a3231131a8a94fd3eaf64df4c`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f718a2a569cddb414e88527a1c82a5249ef00ed13d6d969d03fd6fe947be4b0`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877f61b5788c314f1cac1b07c0313c5527bc575bcd4d8b3272428ee623f3b274`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23f9c5dc2c1283e409e70ca0d2b4a332c5801dc25dc5843d1757ab106ed8c0`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b1f9791b335c7b2bb6a757c468f291e693c2ccdf3877d6824d897eb61a4d54df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520c66be7ff520149482f170959560d0ba42369cac8764a5c7a7f77c5508bca8`

```dockerfile
```

-	Layers:
	-	`sha256:eeb9d59564585bc42c45673ed7070fabc5908a173de9834f878eda77da97e602`  
		Last Modified: Tue, 21 Jan 2025 21:07:25 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f8f084af66dcc16af366577ae5c690b03d7cfac9e61cd0f96b8059a0fb45b973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124682037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540a5c12b45b516c76d8ea89c3597f0793e3798019bddf32d002d8f5ea5c33a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ac6636f9483ab54616b64903f8ba8d2cccee9440eb895c78d56ace8d3e4f96`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 6.4 MB (6367540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5348b12a83f89cbde850839c9f9cbbcb324c91ba1d7f5c1a142a6b282380fa8`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 85.2 KB (85240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eec605d713ebdd1bfff3c3503cc918cb50f85ece729d9770a8209d44099ddb7`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf469db7797818d99b9e99e927b899189f5993e54bb858b340b9eb4e3900a771`  
		Last Modified: Tue, 21 Jan 2025 21:07:31 GMT  
		Size: 54.0 MB (54047072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8360a16ab6657a3443418100cf468a24ee74c8c7e9eaa7582055fe8081c0140`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25fdd4000a14fc00def0dfdc4c82344e1c846243be32bb60c28b8d110b744d`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3c7af3642f4779bc4148276b9902201860a53549bb11720b590ae5017cba85bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbf80603931802b71715d79b520e20f5ed851543f67792da506a4a5b901f599`

```dockerfile
```

-	Layers:
	-	`sha256:b8f59cb6e5ce03d8cfe1900ab25b26a4611e555e10cd4f04345b772825949593`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-dind-rootless`

```console
$ docker pull docker@sha256:5894f4cff8223ed0e1cfcab0d451849166a27cf9bd88bf7d83c53bb0bdad775c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ebd049ca6195b27ec4d34483b4e38e88515c9bfeb884537a44f08a2fe05d5f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157613241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6353ec2f724bd821b6dd3bcad22c0c0213128ff2c9331f636c702b4dd81afe40`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2030ef23a285bdccc40ad0b8ce9efd335fa61d75066bd807c3c82aeac0f5f88`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 986.6 KB (986595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061b18067d315bf70f729ee154e161b68bbe16810de94c1d627a4c781f721c3f`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2867fc390a21dec4f2ebdbb9300bf3927b4896771538473397c8af0916a37254`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0483bcb96635778b03e6a5ff71821e008f3b7ce018ce583db4445025063d703`  
		Last Modified: Wed, 22 Jan 2025 21:10:25 GMT  
		Size: 21.3 MB (21319725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b23e1fe72a9f72a4cf162d1c5061014d374dacd1d4100f237be5d25a322a`  
		Last Modified: Wed, 22 Jan 2025 21:10:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f55d62345aa0a7d862bbd0b6823a21e050a79f4e9d5e6d5d65e4c49e4574c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e295f522e42b2f55e6fd395f80567bc863c970e296904d50e89e25eb29e3000f`

```dockerfile
```

-	Layers:
	-	`sha256:35de99a4851778ee6250f309e86dae0f1fb8984bdcbc582760697bcf74974b11`  
		Last Modified: Wed, 22 Jan 2025 21:10:23 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:833312f4f1a9ef7036f2eb35dc25b09b976770a5326fe1ae0c2eff1694329dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151181458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa2e4d37c474367c7177f81b11d61750fde80a813648fb40a7fba203a66a14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b727576946f5ef0ee11736742c4ff0470a45828e4ce130d8e5158a71cdc4515a`  
		Last Modified: Tue, 21 Jan 2025 20:44:26 GMT  
		Size: 8.1 MB (8074424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2959c0b73dae5e70c97573b56c908480cc4794318911d7610b30a7d08add5e67`  
		Last Modified: Tue, 21 Jan 2025 20:44:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9d6033bb3f386bb327c2a9dea343cefc26aeb5b2e417d7c983657640216e63`  
		Last Modified: Tue, 21 Jan 2025 20:44:26 GMT  
		Size: 17.8 MB (17795758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71047f9f9e392480cc32ed9ac2fc6ed8585cce97a79dc96a0930c972f75ca660`  
		Last Modified: Tue, 21 Jan 2025 20:44:26 GMT  
		Size: 18.5 MB (18458817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b817e8d2b390c439babdc0043d6cf2b5759fb141bd00c9afda6079131e738`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c318310707fb7d70580473eefb15f5bafd42ed152cffed011782dea9d4f3c0`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07193a6ec91b4162516067c96e1ef0e311d7040662f575641cfd216ba9fb1b6f`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508661da5f6d786932535a6222a1c9ab8241662fa84c4aa1fe7f0e696bb814dd`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aeabb3b339362e97bb858dde3992bea728a71c3383d745f93e427151713b6c7`  
		Last Modified: Tue, 21 Jan 2025 21:07:33 GMT  
		Size: 7.0 MB (6981856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c10601a92c5b122e04503bcb1e83c4f3f82a117bc4e728e37b9e391f59211f9`  
		Last Modified: Tue, 21 Jan 2025 21:07:32 GMT  
		Size: 97.8 KB (97787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f958e3424c382e9adc12d77fcbbd8874e403b5b88b7c90902a67d15c890e59`  
		Last Modified: Tue, 21 Jan 2025 21:07:32 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e6227060ad9047fcb92528e802e2346e3dd60dc992edf63a3d4d013ead61e6`  
		Last Modified: Tue, 21 Jan 2025 21:07:34 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4f193ab21aed60d8c9fec5613d685cb40335600aa233556a06505e0ef5318`  
		Last Modified: Tue, 21 Jan 2025 21:07:33 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759900d45cbe5d399f81c58532e5522310c16f03afe794a0bf3a50b5fd054c77`  
		Last Modified: Tue, 21 Jan 2025 21:07:33 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cb4aa93ab603e4d4d33d7d2d3f82369c3e359048c6fdb08875b0afb9cc03dc`  
		Last Modified: Tue, 21 Jan 2025 22:26:04 GMT  
		Size: 1.0 MB (1014210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e90b89b9be7fcda0f00b817afa36b2749564c4e99751d5c7058e402b66bf48b`  
		Last Modified: Tue, 21 Jan 2025 22:26:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0513e4ce7390c12c9bc93c6159f762dfe4f7e3c360539df0d7cf96de1707f108`  
		Last Modified: Tue, 21 Jan 2025 22:26:06 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e28a5e173d0d71747307dbbe2bb458536d5a9afe7d6ec4763579c7263115aa`  
		Last Modified: Tue, 21 Jan 2025 22:26:08 GMT  
		Size: 23.2 MB (23155149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeb43a8221adfbb3e388e9580b0ba5a29a4333f64965bc4faaa84858ecf1cce`  
		Last Modified: Tue, 21 Jan 2025 22:26:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:caead8335948168299f106e6d8abf4c8bb107a57c7bd57a767a7632ff3de974b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d57ab7f48c566a66a83a0468613379b200f3ca872f028c4dca41036e58ac2b3`

```dockerfile
```

-	Layers:
	-	`sha256:2267704e3c4977b5238c0b47cc65ef3aa58a5fc69b1b7e7c49e70fede78cb64e`  
		Last Modified: Tue, 21 Jan 2025 22:26:06 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-windowsservercore`

```console
$ docker pull docker@sha256:b6f8b0d57df4a2696419a5762e577d335b8045344e3955e8f4dbe161e18af19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Thu, 23 Jan 2025 01:33:30 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:5c1a568071d5c38211f0f2ab29165658baa270218a50280ea14a48e551fdb8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323144969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7fa5f72ee91f71047e0cae9811ca6f53ba1a60cdb312db0a9d0345798a4187`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 01:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:28:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:28:53 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:28:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:29:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:29:14 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:29:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed09903d475f8bbfa96b9ead8ead4f2a39d0f719b474586e24a4a58b9470345e`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52dc955ea9bebcaa9ed296818141638ea1aacbed9fdba231dc54b2980b65a5c`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 361.5 KB (361541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a2af8cdcfc4a587bf767381b48afc6c8a51de1f15d8bc0b58ab40283a5f4b`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03fc4d8fe06a92147d6a07ecb5da93751eb8bba0ddcf071c2c3cae0a21b87e3`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb589666dc5302c33e2bd3103275dce7cc6d806c1f7941c8b7d21cfb86111fdc`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 19.1 MB (19134262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a47ad75b95b47fedf86cc1b64b2ee05f4d918b17abd048778f49815048d7510`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38a2eb0cc0556e4da418dfa0ee2cdc500a1f6939268795cfc7257456825f41`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f4b5f8bb28da0ae8bbf98a59430a7a7bc9c34fd58f375b55d628b8b87ab0b7`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c4b941c28c51cd43369ba6156390bdf5fb913aeb0f27ac099875fe7524cae4`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 21.1 MB (21112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d65a4d2b1bb37dc218ab758d1ceee791d50caec34bb6831847c4a8160c67a`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e41bf06ac3da01d5d8fad12e4accd484fedf4eba4a806a136587de0f9b1cda`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ae2d6a0e330b4f2d8f8b93d611370649ad1f85767b559b921a5c1ee27b5bd`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8b1dd36f2eb10913aef8028fb60fb8cd6ef11f7e112ee8ffbbe965253d530`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 20.1 MB (20140156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:38bc4d48f3168306d2d648e0af9406d27bb41a6537d46185c81cefb8ebef842d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183020077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3b61b7f9129666ce834144f71d29ff871f27da200bb6cf5e5f7c0aef7c6ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 01:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:35:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:35:13 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:35:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:35:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:35:29 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:35:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:35:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e1f7a6ddd0af874949fad5fb2b18dc713d63a1972a77488e76118dd264f9d6`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33a1f96da749ae14a963290552db28406e792510359e069b46c86dcf63dc44`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 339.2 KB (339235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72e1a49e563e9bd93904b22396c2cd2f02b470a1bde810aa4003c0ef0ab56`  
		Last Modified: Thu, 23 Jan 2025 01:36:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a932c4224a159c091a14b8d1fe2b1c82bd3a605f046e5770a30f20464d41`  
		Last Modified: Thu, 23 Jan 2025 01:35:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60ccc3c7b375c18d01ab1d49ab7bbe737fc195d6d8e69b61742a296795eb775`  
		Last Modified: Thu, 23 Jan 2025 01:36:01 GMT  
		Size: 19.2 MB (19162080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbc1c67f17e5b2e533cc4d4cbf4892631ec102977971247237ed7b91d36994`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4841f280b69012015b175aa6b6f87bc6d793a6e8d36f300ad59f649531a6d1`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d47b4005db434e43608202c5acadac1e39ac41c7da57dc0ed3db8b450198b6f`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ce7b9a878c3aff2e2a97b385f7c75f6043234bb92a724f5f7c060be0032be1`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 21.1 MB (21130564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd9a849c2c7eefd648403d5cd4e04a259de2927c100bc629bbbb132b5f821c3`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5505d56ad65828edc87e543f61694fe4bc77d3be290c27ecf695f8625ba2c415`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce02b8200d83f1b73eeee2e5797bdb4fe5b87497dea1b31c3a655e45cd8d011c`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042952d001e4adcdab5611fa007695ef67a2707230a2be2278cd1fc6cea222a4`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 20.2 MB (20163992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5-windowsservercore-1809`

```console
$ docker pull docker@sha256:383bafe0d882dfaee478abe15a862e5a2cbd50cef39a1ca7bfa511fdff4053cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:38bc4d48f3168306d2d648e0af9406d27bb41a6537d46185c81cefb8ebef842d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183020077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3b61b7f9129666ce834144f71d29ff871f27da200bb6cf5e5f7c0aef7c6ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 01:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:35:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:35:13 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:35:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:35:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:35:29 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:35:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:35:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e1f7a6ddd0af874949fad5fb2b18dc713d63a1972a77488e76118dd264f9d6`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33a1f96da749ae14a963290552db28406e792510359e069b46c86dcf63dc44`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 339.2 KB (339235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72e1a49e563e9bd93904b22396c2cd2f02b470a1bde810aa4003c0ef0ab56`  
		Last Modified: Thu, 23 Jan 2025 01:36:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a932c4224a159c091a14b8d1fe2b1c82bd3a605f046e5770a30f20464d41`  
		Last Modified: Thu, 23 Jan 2025 01:35:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60ccc3c7b375c18d01ab1d49ab7bbe737fc195d6d8e69b61742a296795eb775`  
		Last Modified: Thu, 23 Jan 2025 01:36:01 GMT  
		Size: 19.2 MB (19162080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbc1c67f17e5b2e533cc4d4cbf4892631ec102977971247237ed7b91d36994`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4841f280b69012015b175aa6b6f87bc6d793a6e8d36f300ad59f649531a6d1`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d47b4005db434e43608202c5acadac1e39ac41c7da57dc0ed3db8b450198b6f`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ce7b9a878c3aff2e2a97b385f7c75f6043234bb92a724f5f7c060be0032be1`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 21.1 MB (21130564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd9a849c2c7eefd648403d5cd4e04a259de2927c100bc629bbbb132b5f821c3`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5505d56ad65828edc87e543f61694fe4bc77d3be290c27ecf695f8625ba2c415`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce02b8200d83f1b73eeee2e5797bdb4fe5b87497dea1b31c3a655e45cd8d011c`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042952d001e4adcdab5611fa007695ef67a2707230a2be2278cd1fc6cea222a4`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 20.2 MB (20163992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c37cf3b88ac15878732da1a35ced92a3889e31d4512d22dac218f03dc9cedb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:27.5-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:5c1a568071d5c38211f0f2ab29165658baa270218a50280ea14a48e551fdb8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323144969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7fa5f72ee91f71047e0cae9811ca6f53ba1a60cdb312db0a9d0345798a4187`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 01:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:28:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:28:53 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:28:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:29:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:29:14 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:29:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed09903d475f8bbfa96b9ead8ead4f2a39d0f719b474586e24a4a58b9470345e`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52dc955ea9bebcaa9ed296818141638ea1aacbed9fdba231dc54b2980b65a5c`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 361.5 KB (361541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a2af8cdcfc4a587bf767381b48afc6c8a51de1f15d8bc0b58ab40283a5f4b`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03fc4d8fe06a92147d6a07ecb5da93751eb8bba0ddcf071c2c3cae0a21b87e3`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb589666dc5302c33e2bd3103275dce7cc6d806c1f7941c8b7d21cfb86111fdc`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 19.1 MB (19134262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a47ad75b95b47fedf86cc1b64b2ee05f4d918b17abd048778f49815048d7510`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38a2eb0cc0556e4da418dfa0ee2cdc500a1f6939268795cfc7257456825f41`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f4b5f8bb28da0ae8bbf98a59430a7a7bc9c34fd58f375b55d628b8b87ab0b7`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c4b941c28c51cd43369ba6156390bdf5fb913aeb0f27ac099875fe7524cae4`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 21.1 MB (21112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d65a4d2b1bb37dc218ab758d1ceee791d50caec34bb6831847c4a8160c67a`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e41bf06ac3da01d5d8fad12e4accd484fedf4eba4a806a136587de0f9b1cda`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ae2d6a0e330b4f2d8f8b93d611370649ad1f85767b559b921a5c1ee27b5bd`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8b1dd36f2eb10913aef8028fb60fb8cd6ef11f7e112ee8ffbbe965253d530`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 20.1 MB (20140156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c68bdfb265f8b44bdcdbd856c52b597a0adc9e70d38d1073c2dcbeb23e26818e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:27.5-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Thu, 23 Jan 2025 01:33:30 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.1`

```console
$ docker pull docker@sha256:b528cb3c896d830cb0ea63159575ec3941bced88a94bd0e1f12cf8bf3653b1ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5.1` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.1-alpine3.21`

```console
$ docker pull docker@sha256:b528cb3c896d830cb0ea63159575ec3941bced88a94bd0e1f12cf8bf3653b1ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5.1-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.1-cli`

```console
$ docker pull docker@sha256:bb4b8a287f8407b9fea1824ba39798b46cd1bf0531680f23e768dd1c86362c79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:e1b7fa9b2d15b445084ecae08fb67d249c7748725a8731e0ef2d5fb5c54dba9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70091097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383208bbb6b0c1a0e235f583f3c8b7f80529e4ba7b91ff4952e988a75e57437b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4543eb003ef94a05439cb5446e2fe5d1a1318a77a5ecd0f7ce0f77bfde1f61`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 8.1 MB (8060130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b66b6f01517380357ef07c7409f00407748f8e744c0eb5ed5efe498c2e5bb`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df855c4e32dd197ba449da2be8641932cbc5879636990104ef951c56eaf1b82`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 18.8 MB (18848905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b6742bd2d5a6242c709b92cf93f22139461e1ff302a6f601fd1cabf1af7580`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 20.2 MB (20234555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af9ba02f40bd06616eacbd5670ba2485bd87a92b4c972cf5bf1120ff27aa1b`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1193bea83fc8c129bcfd73718e8e96feb49527eb743470a8f08e0ccc8a9ec2b3`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae3e6f1bf5bb5465e3db71bb733f3cacc996333fbee14a57bef4eb56ce912`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046ca50013a72571a456c1a5437df9fe09fe9be0f35107d9a6a20518449da42`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:13bf5de648cb5dcec33c01c66cc8cc55752b09fd237dce16215654738d142689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07d5481f565c713cf6c1f3c29a788fe00c89b8ec831200bf121baa5ffc40bde`

```dockerfile
```

-	Layers:
	-	`sha256:d631712da516c7c8bd3f89066d3f8f96905f5d19845d63d390476765e524e735`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:67daf59d1ebdf055fc86f315690f99720fe2e76c422f47c3f15cbd59798a7781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65161798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8395e26813af8fba5ddfef47bb16e82d996373cb799de4b15c2204ffe8725ca3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed4e5240126a237686beb0364732ea8fb90b8222bb79ece3b01bc65f11255f8`  
		Last Modified: Thu, 23 Jan 2025 01:08:51 GMT  
		Size: 16.9 MB (16866758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc64aa21acc52ff9715cac0a1c9950afe80cf8a4ea1a68baec921a635cb58a9b`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.8 MB (18843713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac9ccf0752d89cd64424f0e836d6a53bcf608d2ade5c57f9e268310298d7c8`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.1 MB (18112376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee11d500ae760463d5de6d7e1832499db3e5428c8aa304592b37e53e49d17d5`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e7eeefb54f6e84b1a476d04890600e732afcfbb674962f1d0af1f84c3b20f8`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089baa8d0b7e233427ebf7a6ec651326f37ce677522489b2445fa3a8ddf54820`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5b461226ce2d9537eecdcd27c8103b253c6453c497ac8b2c67e62f43b19e4651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769dd3e9bae0849e1af06e8b2ed0bb521e30956eb80ad18e01d1fbd4072b8976`

```dockerfile
```

-	Layers:
	-	`sha256:0a463fb4d15db5c2a23b7371f79cc40b855f69ffe02bd964e646b412a881d150`  
		Last Modified: Thu, 23 Jan 2025 01:28:08 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6f1a1a24027716e44d9b7a08b7252bf33c60403dd92c77bf863d625a15bf302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65972403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581c2c02c852d766afb66b604dbd45f44c1bdd42eb5cb2c127663c9e3954b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d47d71a04452163577e439ccf4d91457ac4ab2f7fa68cc32517b973eae562185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bbc8c969ef865647e5cf02166f155e554bf917314e431725c57c35399e34f1`

```dockerfile
```

-	Layers:
	-	`sha256:15793555fc85eacaeec2b45b37d648b58e45b2ba5fcb0e42884c619c7eb12885`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.1-cli-alpine3.21`

```console
$ docker pull docker@sha256:bb4b8a287f8407b9fea1824ba39798b46cd1bf0531680f23e768dd1c86362c79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5.1-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:e1b7fa9b2d15b445084ecae08fb67d249c7748725a8731e0ef2d5fb5c54dba9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70091097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383208bbb6b0c1a0e235f583f3c8b7f80529e4ba7b91ff4952e988a75e57437b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4543eb003ef94a05439cb5446e2fe5d1a1318a77a5ecd0f7ce0f77bfde1f61`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 8.1 MB (8060130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b66b6f01517380357ef07c7409f00407748f8e744c0eb5ed5efe498c2e5bb`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df855c4e32dd197ba449da2be8641932cbc5879636990104ef951c56eaf1b82`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 18.8 MB (18848905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b6742bd2d5a6242c709b92cf93f22139461e1ff302a6f601fd1cabf1af7580`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 20.2 MB (20234555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af9ba02f40bd06616eacbd5670ba2485bd87a92b4c972cf5bf1120ff27aa1b`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1193bea83fc8c129bcfd73718e8e96feb49527eb743470a8f08e0ccc8a9ec2b3`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae3e6f1bf5bb5465e3db71bb733f3cacc996333fbee14a57bef4eb56ce912`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046ca50013a72571a456c1a5437df9fe09fe9be0f35107d9a6a20518449da42`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:13bf5de648cb5dcec33c01c66cc8cc55752b09fd237dce16215654738d142689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07d5481f565c713cf6c1f3c29a788fe00c89b8ec831200bf121baa5ffc40bde`

```dockerfile
```

-	Layers:
	-	`sha256:d631712da516c7c8bd3f89066d3f8f96905f5d19845d63d390476765e524e735`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.1-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:67daf59d1ebdf055fc86f315690f99720fe2e76c422f47c3f15cbd59798a7781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65161798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8395e26813af8fba5ddfef47bb16e82d996373cb799de4b15c2204ffe8725ca3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed4e5240126a237686beb0364732ea8fb90b8222bb79ece3b01bc65f11255f8`  
		Last Modified: Thu, 23 Jan 2025 01:08:51 GMT  
		Size: 16.9 MB (16866758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc64aa21acc52ff9715cac0a1c9950afe80cf8a4ea1a68baec921a635cb58a9b`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.8 MB (18843713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac9ccf0752d89cd64424f0e836d6a53bcf608d2ade5c57f9e268310298d7c8`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.1 MB (18112376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee11d500ae760463d5de6d7e1832499db3e5428c8aa304592b37e53e49d17d5`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e7eeefb54f6e84b1a476d04890600e732afcfbb674962f1d0af1f84c3b20f8`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089baa8d0b7e233427ebf7a6ec651326f37ce677522489b2445fa3a8ddf54820`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:5b461226ce2d9537eecdcd27c8103b253c6453c497ac8b2c67e62f43b19e4651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769dd3e9bae0849e1af06e8b2ed0bb521e30956eb80ad18e01d1fbd4072b8976`

```dockerfile
```

-	Layers:
	-	`sha256:0a463fb4d15db5c2a23b7371f79cc40b855f69ffe02bd964e646b412a881d150`  
		Last Modified: Thu, 23 Jan 2025 01:28:08 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.1-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6f1a1a24027716e44d9b7a08b7252bf33c60403dd92c77bf863d625a15bf302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65972403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581c2c02c852d766afb66b604dbd45f44c1bdd42eb5cb2c127663c9e3954b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:d47d71a04452163577e439ccf4d91457ac4ab2f7fa68cc32517b973eae562185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bbc8c969ef865647e5cf02166f155e554bf917314e431725c57c35399e34f1`

```dockerfile
```

-	Layers:
	-	`sha256:15793555fc85eacaeec2b45b37d648b58e45b2ba5fcb0e42884c619c7eb12885`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.1-dind`

```console
$ docker pull docker@sha256:b528cb3c896d830cb0ea63159575ec3941bced88a94bd0e1f12cf8bf3653b1ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.1-dind-alpine3.21`

```console
$ docker pull docker@sha256:b528cb3c896d830cb0ea63159575ec3941bced88a94bd0e1f12cf8bf3653b1ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5.1-dind-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.1-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.1-dind-rootless`

```console
$ docker pull docker@sha256:5cdc520ce688c60bb6fc944a5850e7a63da498b4d31d706b5c0ed5a23e5e97d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `docker:27.5.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ebd049ca6195b27ec4d34483b4e38e88515c9bfeb884537a44f08a2fe05d5f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157613241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6353ec2f724bd821b6dd3bcad22c0c0213128ff2c9331f636c702b4dd81afe40`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2030ef23a285bdccc40ad0b8ce9efd335fa61d75066bd807c3c82aeac0f5f88`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 986.6 KB (986595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061b18067d315bf70f729ee154e161b68bbe16810de94c1d627a4c781f721c3f`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2867fc390a21dec4f2ebdbb9300bf3927b4896771538473397c8af0916a37254`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0483bcb96635778b03e6a5ff71821e008f3b7ce018ce583db4445025063d703`  
		Last Modified: Wed, 22 Jan 2025 21:10:25 GMT  
		Size: 21.3 MB (21319725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b23e1fe72a9f72a4cf162d1c5061014d374dacd1d4100f237be5d25a322a`  
		Last Modified: Wed, 22 Jan 2025 21:10:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f55d62345aa0a7d862bbd0b6823a21e050a79f4e9d5e6d5d65e4c49e4574c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e295f522e42b2f55e6fd395f80567bc863c970e296904d50e89e25eb29e3000f`

```dockerfile
```

-	Layers:
	-	`sha256:35de99a4851778ee6250f309e86dae0f1fb8984bdcbc582760697bcf74974b11`  
		Last Modified: Wed, 22 Jan 2025 21:10:23 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.1-windowsservercore`

```console
$ docker pull docker@sha256:b6f8b0d57df4a2696419a5762e577d335b8045344e3955e8f4dbe161e18af19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5.1-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Thu, 23 Jan 2025 01:33:30 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5.1-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:5c1a568071d5c38211f0f2ab29165658baa270218a50280ea14a48e551fdb8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323144969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7fa5f72ee91f71047e0cae9811ca6f53ba1a60cdb312db0a9d0345798a4187`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 01:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:28:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:28:53 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:28:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:29:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:29:14 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:29:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed09903d475f8bbfa96b9ead8ead4f2a39d0f719b474586e24a4a58b9470345e`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52dc955ea9bebcaa9ed296818141638ea1aacbed9fdba231dc54b2980b65a5c`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 361.5 KB (361541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a2af8cdcfc4a587bf767381b48afc6c8a51de1f15d8bc0b58ab40283a5f4b`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03fc4d8fe06a92147d6a07ecb5da93751eb8bba0ddcf071c2c3cae0a21b87e3`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb589666dc5302c33e2bd3103275dce7cc6d806c1f7941c8b7d21cfb86111fdc`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 19.1 MB (19134262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a47ad75b95b47fedf86cc1b64b2ee05f4d918b17abd048778f49815048d7510`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38a2eb0cc0556e4da418dfa0ee2cdc500a1f6939268795cfc7257456825f41`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f4b5f8bb28da0ae8bbf98a59430a7a7bc9c34fd58f375b55d628b8b87ab0b7`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c4b941c28c51cd43369ba6156390bdf5fb913aeb0f27ac099875fe7524cae4`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 21.1 MB (21112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d65a4d2b1bb37dc218ab758d1ceee791d50caec34bb6831847c4a8160c67a`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e41bf06ac3da01d5d8fad12e4accd484fedf4eba4a806a136587de0f9b1cda`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ae2d6a0e330b4f2d8f8b93d611370649ad1f85767b559b921a5c1ee27b5bd`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8b1dd36f2eb10913aef8028fb60fb8cd6ef11f7e112ee8ffbbe965253d530`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 20.1 MB (20140156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5.1-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:38bc4d48f3168306d2d648e0af9406d27bb41a6537d46185c81cefb8ebef842d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183020077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3b61b7f9129666ce834144f71d29ff871f27da200bb6cf5e5f7c0aef7c6ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 01:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:35:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:35:13 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:35:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:35:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:35:29 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:35:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:35:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e1f7a6ddd0af874949fad5fb2b18dc713d63a1972a77488e76118dd264f9d6`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33a1f96da749ae14a963290552db28406e792510359e069b46c86dcf63dc44`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 339.2 KB (339235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72e1a49e563e9bd93904b22396c2cd2f02b470a1bde810aa4003c0ef0ab56`  
		Last Modified: Thu, 23 Jan 2025 01:36:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a932c4224a159c091a14b8d1fe2b1c82bd3a605f046e5770a30f20464d41`  
		Last Modified: Thu, 23 Jan 2025 01:35:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60ccc3c7b375c18d01ab1d49ab7bbe737fc195d6d8e69b61742a296795eb775`  
		Last Modified: Thu, 23 Jan 2025 01:36:01 GMT  
		Size: 19.2 MB (19162080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbc1c67f17e5b2e533cc4d4cbf4892631ec102977971247237ed7b91d36994`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4841f280b69012015b175aa6b6f87bc6d793a6e8d36f300ad59f649531a6d1`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d47b4005db434e43608202c5acadac1e39ac41c7da57dc0ed3db8b450198b6f`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ce7b9a878c3aff2e2a97b385f7c75f6043234bb92a724f5f7c060be0032be1`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 21.1 MB (21130564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd9a849c2c7eefd648403d5cd4e04a259de2927c100bc629bbbb132b5f821c3`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5505d56ad65828edc87e543f61694fe4bc77d3be290c27ecf695f8625ba2c415`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce02b8200d83f1b73eeee2e5797bdb4fe5b87497dea1b31c3a655e45cd8d011c`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042952d001e4adcdab5611fa007695ef67a2707230a2be2278cd1fc6cea222a4`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 20.2 MB (20163992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:383bafe0d882dfaee478abe15a862e5a2cbd50cef39a1ca7bfa511fdff4053cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5.1-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:38bc4d48f3168306d2d648e0af9406d27bb41a6537d46185c81cefb8ebef842d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183020077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3b61b7f9129666ce834144f71d29ff871f27da200bb6cf5e5f7c0aef7c6ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 01:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:35:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:35:13 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:35:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:35:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:35:29 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:35:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:35:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e1f7a6ddd0af874949fad5fb2b18dc713d63a1972a77488e76118dd264f9d6`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33a1f96da749ae14a963290552db28406e792510359e069b46c86dcf63dc44`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 339.2 KB (339235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72e1a49e563e9bd93904b22396c2cd2f02b470a1bde810aa4003c0ef0ab56`  
		Last Modified: Thu, 23 Jan 2025 01:36:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a932c4224a159c091a14b8d1fe2b1c82bd3a605f046e5770a30f20464d41`  
		Last Modified: Thu, 23 Jan 2025 01:35:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60ccc3c7b375c18d01ab1d49ab7bbe737fc195d6d8e69b61742a296795eb775`  
		Last Modified: Thu, 23 Jan 2025 01:36:01 GMT  
		Size: 19.2 MB (19162080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbc1c67f17e5b2e533cc4d4cbf4892631ec102977971247237ed7b91d36994`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4841f280b69012015b175aa6b6f87bc6d793a6e8d36f300ad59f649531a6d1`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d47b4005db434e43608202c5acadac1e39ac41c7da57dc0ed3db8b450198b6f`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ce7b9a878c3aff2e2a97b385f7c75f6043234bb92a724f5f7c060be0032be1`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 21.1 MB (21130564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd9a849c2c7eefd648403d5cd4e04a259de2927c100bc629bbbb132b5f821c3`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5505d56ad65828edc87e543f61694fe4bc77d3be290c27ecf695f8625ba2c415`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce02b8200d83f1b73eeee2e5797bdb4fe5b87497dea1b31c3a655e45cd8d011c`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042952d001e4adcdab5611fa007695ef67a2707230a2be2278cd1fc6cea222a4`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 20.2 MB (20163992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c37cf3b88ac15878732da1a35ced92a3889e31d4512d22dac218f03dc9cedb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:27.5.1-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:5c1a568071d5c38211f0f2ab29165658baa270218a50280ea14a48e551fdb8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323144969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7fa5f72ee91f71047e0cae9811ca6f53ba1a60cdb312db0a9d0345798a4187`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 01:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:28:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:28:53 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:28:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:29:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:29:14 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:29:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed09903d475f8bbfa96b9ead8ead4f2a39d0f719b474586e24a4a58b9470345e`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52dc955ea9bebcaa9ed296818141638ea1aacbed9fdba231dc54b2980b65a5c`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 361.5 KB (361541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a2af8cdcfc4a587bf767381b48afc6c8a51de1f15d8bc0b58ab40283a5f4b`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03fc4d8fe06a92147d6a07ecb5da93751eb8bba0ddcf071c2c3cae0a21b87e3`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb589666dc5302c33e2bd3103275dce7cc6d806c1f7941c8b7d21cfb86111fdc`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 19.1 MB (19134262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a47ad75b95b47fedf86cc1b64b2ee05f4d918b17abd048778f49815048d7510`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38a2eb0cc0556e4da418dfa0ee2cdc500a1f6939268795cfc7257456825f41`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f4b5f8bb28da0ae8bbf98a59430a7a7bc9c34fd58f375b55d628b8b87ab0b7`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c4b941c28c51cd43369ba6156390bdf5fb913aeb0f27ac099875fe7524cae4`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 21.1 MB (21112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d65a4d2b1bb37dc218ab758d1ceee791d50caec34bb6831847c4a8160c67a`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e41bf06ac3da01d5d8fad12e4accd484fedf4eba4a806a136587de0f9b1cda`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ae2d6a0e330b4f2d8f8b93d611370649ad1f85767b559b921a5c1ee27b5bd`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8b1dd36f2eb10913aef8028fb60fb8cd6ef11f7e112ee8ffbbe965253d530`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 20.1 MB (20140156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c68bdfb265f8b44bdcdbd856c52b597a0adc9e70d38d1073c2dcbeb23e26818e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:27.5.1-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Thu, 23 Jan 2025 01:33:30 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:1d07d717b4bce04c3446175b3d4bd6c7c16567fd8f061e992ad6c28f2d49054e
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

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:e1b7fa9b2d15b445084ecae08fb67d249c7748725a8731e0ef2d5fb5c54dba9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70091097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383208bbb6b0c1a0e235f583f3c8b7f80529e4ba7b91ff4952e988a75e57437b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4543eb003ef94a05439cb5446e2fe5d1a1318a77a5ecd0f7ce0f77bfde1f61`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 8.1 MB (8060130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b66b6f01517380357ef07c7409f00407748f8e744c0eb5ed5efe498c2e5bb`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df855c4e32dd197ba449da2be8641932cbc5879636990104ef951c56eaf1b82`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 18.8 MB (18848905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b6742bd2d5a6242c709b92cf93f22139461e1ff302a6f601fd1cabf1af7580`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 20.2 MB (20234555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af9ba02f40bd06616eacbd5670ba2485bd87a92b4c972cf5bf1120ff27aa1b`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1193bea83fc8c129bcfd73718e8e96feb49527eb743470a8f08e0ccc8a9ec2b3`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae3e6f1bf5bb5465e3db71bb733f3cacc996333fbee14a57bef4eb56ce912`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046ca50013a72571a456c1a5437df9fe09fe9be0f35107d9a6a20518449da42`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:13bf5de648cb5dcec33c01c66cc8cc55752b09fd237dce16215654738d142689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07d5481f565c713cf6c1f3c29a788fe00c89b8ec831200bf121baa5ffc40bde`

```dockerfile
```

-	Layers:
	-	`sha256:d631712da516c7c8bd3f89066d3f8f96905f5d19845d63d390476765e524e735`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:67daf59d1ebdf055fc86f315690f99720fe2e76c422f47c3f15cbd59798a7781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65161798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8395e26813af8fba5ddfef47bb16e82d996373cb799de4b15c2204ffe8725ca3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed4e5240126a237686beb0364732ea8fb90b8222bb79ece3b01bc65f11255f8`  
		Last Modified: Thu, 23 Jan 2025 01:08:51 GMT  
		Size: 16.9 MB (16866758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc64aa21acc52ff9715cac0a1c9950afe80cf8a4ea1a68baec921a635cb58a9b`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.8 MB (18843713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac9ccf0752d89cd64424f0e836d6a53bcf608d2ade5c57f9e268310298d7c8`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.1 MB (18112376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee11d500ae760463d5de6d7e1832499db3e5428c8aa304592b37e53e49d17d5`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e7eeefb54f6e84b1a476d04890600e732afcfbb674962f1d0af1f84c3b20f8`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089baa8d0b7e233427ebf7a6ec651326f37ce677522489b2445fa3a8ddf54820`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:5b461226ce2d9537eecdcd27c8103b253c6453c497ac8b2c67e62f43b19e4651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769dd3e9bae0849e1af06e8b2ed0bb521e30956eb80ad18e01d1fbd4072b8976`

```dockerfile
```

-	Layers:
	-	`sha256:0a463fb4d15db5c2a23b7371f79cc40b855f69ffe02bd964e646b412a881d150`  
		Last Modified: Thu, 23 Jan 2025 01:28:08 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:0091be5184eae4250fc1cb11a01fe5ea066d1b7a846c67a6d23e817d010260a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64176388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7773e8edbbc039cd622aa68e12968928793e28dc0fd375c732981a7e42162a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 21 Jan 2025 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:d503a1f6ea902951cfe37f5418137ffcd9c643beb7df1964bd2e45c83ef6f07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d161766fb8c4a9cb705ff2b79fe8c2fc98c84779426e81316089633605422d`

```dockerfile
```

-	Layers:
	-	`sha256:79bd3d5210a7b1bf892a818f3142ff8a95fb47d2845f0667fb2b28d4ed3d1b6b`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6f1a1a24027716e44d9b7a08b7252bf33c60403dd92c77bf863d625a15bf302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65972403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581c2c02c852d766afb66b604dbd45f44c1bdd42eb5cb2c127663c9e3954b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:d47d71a04452163577e439ccf4d91457ac4ab2f7fa68cc32517b973eae562185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bbc8c969ef865647e5cf02166f155e554bf917314e431725c57c35399e34f1`

```dockerfile
```

-	Layers:
	-	`sha256:15793555fc85eacaeec2b45b37d648b58e45b2ba5fcb0e42884c619c7eb12885`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:886e39f1390baaa74778366b228fc809ed8815a9235809ff8d2b038fdef0d09c
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

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:5abfa3c0ff7d4add4395054751775d599a196874df408ea032b3892af0c2adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126344304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aef0003a941f9ed6335047bc2741dd2c754246e44b792596444ba505425924b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06b3967b4e642b2d6cb98ddda55dabc4993a3899194dfb50645801f28a2de4d`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.8 MB (18843467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e167d9a57b137b11ef1469f2536ba9c09315dd6e1858686fed99b317c474b`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.1 MB (18112380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746625955b5ebca8aee1d3e40c90c535484d1d6e5dcb2f3af36d50293db19d9b`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778bb8e57da23192256e4be8f68202f6916ae3d97cd410afd26a12c5157d2351`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f6729763aa7494d8f2673d92eaee47a0d1ff164b4022dad21403edbb87ac5`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143d81c732b89ee68c6854c26f60e4bd650052ccaa846e89b879dfd55f47d1e`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 7.0 MB (7041332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70697f77c3da37666380be4a8d5152894d73539601f5b1d05f7f6dfecbafdf40`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 89.1 KB (89095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462068e1d900fc5901c6341ff059c1d41259179a3231131a8a94fd3eaf64df4c`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f718a2a569cddb414e88527a1c82a5249ef00ed13d6d969d03fd6fe947be4b0`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877f61b5788c314f1cac1b07c0313c5527bc575bcd4d8b3272428ee623f3b274`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23f9c5dc2c1283e409e70ca0d2b4a332c5801dc25dc5843d1757ab106ed8c0`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b1f9791b335c7b2bb6a757c468f291e693c2ccdf3877d6824d897eb61a4d54df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520c66be7ff520149482f170959560d0ba42369cac8764a5c7a7f77c5508bca8`

```dockerfile
```

-	Layers:
	-	`sha256:eeb9d59564585bc42c45673ed7070fabc5908a173de9834f878eda77da97e602`  
		Last Modified: Tue, 21 Jan 2025 21:07:25 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f8f084af66dcc16af366577ae5c690b03d7cfac9e61cd0f96b8059a0fb45b973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124682037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540a5c12b45b516c76d8ea89c3597f0793e3798019bddf32d002d8f5ea5c33a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ac6636f9483ab54616b64903f8ba8d2cccee9440eb895c78d56ace8d3e4f96`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 6.4 MB (6367540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5348b12a83f89cbde850839c9f9cbbcb324c91ba1d7f5c1a142a6b282380fa8`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 85.2 KB (85240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eec605d713ebdd1bfff3c3503cc918cb50f85ece729d9770a8209d44099ddb7`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf469db7797818d99b9e99e927b899189f5993e54bb858b340b9eb4e3900a771`  
		Last Modified: Tue, 21 Jan 2025 21:07:31 GMT  
		Size: 54.0 MB (54047072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8360a16ab6657a3443418100cf468a24ee74c8c7e9eaa7582055fe8081c0140`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25fdd4000a14fc00def0dfdc4c82344e1c846243be32bb60c28b8d110b744d`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3c7af3642f4779bc4148276b9902201860a53549bb11720b590ae5017cba85bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbf80603931802b71715d79b520e20f5ed851543f67792da506a4a5b901f599`

```dockerfile
```

-	Layers:
	-	`sha256:b8f59cb6e5ce03d8cfe1900ab25b26a4611e555e10cd4f04345b772825949593`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:5894f4cff8223ed0e1cfcab0d451849166a27cf9bd88bf7d83c53bb0bdad775c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ebd049ca6195b27ec4d34483b4e38e88515c9bfeb884537a44f08a2fe05d5f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157613241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6353ec2f724bd821b6dd3bcad22c0c0213128ff2c9331f636c702b4dd81afe40`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2030ef23a285bdccc40ad0b8ce9efd335fa61d75066bd807c3c82aeac0f5f88`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 986.6 KB (986595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061b18067d315bf70f729ee154e161b68bbe16810de94c1d627a4c781f721c3f`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2867fc390a21dec4f2ebdbb9300bf3927b4896771538473397c8af0916a37254`  
		Last Modified: Wed, 22 Jan 2025 21:10:24 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0483bcb96635778b03e6a5ff71821e008f3b7ce018ce583db4445025063d703`  
		Last Modified: Wed, 22 Jan 2025 21:10:25 GMT  
		Size: 21.3 MB (21319725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b23e1fe72a9f72a4cf162d1c5061014d374dacd1d4100f237be5d25a322a`  
		Last Modified: Wed, 22 Jan 2025 21:10:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f55d62345aa0a7d862bbd0b6823a21e050a79f4e9d5e6d5d65e4c49e4574c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e295f522e42b2f55e6fd395f80567bc863c970e296904d50e89e25eb29e3000f`

```dockerfile
```

-	Layers:
	-	`sha256:35de99a4851778ee6250f309e86dae0f1fb8984bdcbc582760697bcf74974b11`  
		Last Modified: Wed, 22 Jan 2025 21:10:23 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:833312f4f1a9ef7036f2eb35dc25b09b976770a5326fe1ae0c2eff1694329dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151181458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa2e4d37c474367c7177f81b11d61750fde80a813648fb40a7fba203a66a14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b727576946f5ef0ee11736742c4ff0470a45828e4ce130d8e5158a71cdc4515a`  
		Last Modified: Tue, 21 Jan 2025 20:44:26 GMT  
		Size: 8.1 MB (8074424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2959c0b73dae5e70c97573b56c908480cc4794318911d7610b30a7d08add5e67`  
		Last Modified: Tue, 21 Jan 2025 20:44:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9d6033bb3f386bb327c2a9dea343cefc26aeb5b2e417d7c983657640216e63`  
		Last Modified: Tue, 21 Jan 2025 20:44:26 GMT  
		Size: 17.8 MB (17795758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71047f9f9e392480cc32ed9ac2fc6ed8585cce97a79dc96a0930c972f75ca660`  
		Last Modified: Tue, 21 Jan 2025 20:44:26 GMT  
		Size: 18.5 MB (18458817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b817e8d2b390c439babdc0043d6cf2b5759fb141bd00c9afda6079131e738`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c318310707fb7d70580473eefb15f5bafd42ed152cffed011782dea9d4f3c0`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07193a6ec91b4162516067c96e1ef0e311d7040662f575641cfd216ba9fb1b6f`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508661da5f6d786932535a6222a1c9ab8241662fa84c4aa1fe7f0e696bb814dd`  
		Last Modified: Tue, 21 Jan 2025 20:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aeabb3b339362e97bb858dde3992bea728a71c3383d745f93e427151713b6c7`  
		Last Modified: Tue, 21 Jan 2025 21:07:33 GMT  
		Size: 7.0 MB (6981856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c10601a92c5b122e04503bcb1e83c4f3f82a117bc4e728e37b9e391f59211f9`  
		Last Modified: Tue, 21 Jan 2025 21:07:32 GMT  
		Size: 97.8 KB (97787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f958e3424c382e9adc12d77fcbbd8874e403b5b88b7c90902a67d15c890e59`  
		Last Modified: Tue, 21 Jan 2025 21:07:32 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e6227060ad9047fcb92528e802e2346e3dd60dc992edf63a3d4d013ead61e6`  
		Last Modified: Tue, 21 Jan 2025 21:07:34 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4f193ab21aed60d8c9fec5613d685cb40335600aa233556a06505e0ef5318`  
		Last Modified: Tue, 21 Jan 2025 21:07:33 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759900d45cbe5d399f81c58532e5522310c16f03afe794a0bf3a50b5fd054c77`  
		Last Modified: Tue, 21 Jan 2025 21:07:33 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cb4aa93ab603e4d4d33d7d2d3f82369c3e359048c6fdb08875b0afb9cc03dc`  
		Last Modified: Tue, 21 Jan 2025 22:26:04 GMT  
		Size: 1.0 MB (1014210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e90b89b9be7fcda0f00b817afa36b2749564c4e99751d5c7058e402b66bf48b`  
		Last Modified: Tue, 21 Jan 2025 22:26:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0513e4ce7390c12c9bc93c6159f762dfe4f7e3c360539df0d7cf96de1707f108`  
		Last Modified: Tue, 21 Jan 2025 22:26:06 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e28a5e173d0d71747307dbbe2bb458536d5a9afe7d6ec4763579c7263115aa`  
		Last Modified: Tue, 21 Jan 2025 22:26:08 GMT  
		Size: 23.2 MB (23155149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeb43a8221adfbb3e388e9580b0ba5a29a4333f64965bc4faaa84858ecf1cce`  
		Last Modified: Tue, 21 Jan 2025 22:26:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:caead8335948168299f106e6d8abf4c8bb107a57c7bd57a767a7632ff3de974b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d57ab7f48c566a66a83a0468613379b200f3ca872f028c4dca41036e58ac2b3`

```dockerfile
```

-	Layers:
	-	`sha256:2267704e3c4977b5238c0b47cc65ef3aa58a5fc69b1b7e7c49e70fede78cb64e`  
		Last Modified: Tue, 21 Jan 2025 22:26:06 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:886e39f1390baaa74778366b228fc809ed8815a9235809ff8d2b038fdef0d09c
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

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:ee8f5f36acdc18e121d2f38c7438e8ff15c313a7cd239a9a48aca408bd5730c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135305574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47eedab7a4f146279bec158ccb3fd61ddb43f0abc4b6fcb42fd08b3043c023`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc1b6637c51990464eb1c48376e596efd4309ba9ad0e3605d9d5e4699991a2`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 6.7 MB (6733559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988caa0bd686f0860ef7e765b2ff72ea0c8f4f699b96b5a49c9d8ac6a1ad259`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1938c10184e883fea2aa20600725872bc2f2a3d94be3d02c36de08b4f61555`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836eec01f903766a5583cbd6446c1d9b628752567b5bf7542af8609b383af7a9`  
		Last Modified: Wed, 22 Jan 2025 20:31:33 GMT  
		Size: 58.4 MB (58385803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cf6f5747367251f0771d610a9c10c811ce107e640d3463ab9b6342542e219`  
		Last Modified: Wed, 22 Jan 2025 20:31:30 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19416d43ecc14a7c326354bfa8e247a605afea3500714a515d2d1107b2a3a0f`  
		Last Modified: Wed, 22 Jan 2025 20:31:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:4c3df86b605e4af79e1a53811bf9b8bfe41147d4e343f821088c322cfe765c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c88eecb1c2dc646ebffbaefacd80f1a4a464dbdfe074ade09485441029aa7`

```dockerfile
```

-	Layers:
	-	`sha256:24203030359505bcea4aabaeeac9d30a548237e78aad0cd85273d029a4bdfe64`  
		Last Modified: Wed, 22 Jan 2025 20:31:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:5abfa3c0ff7d4add4395054751775d599a196874df408ea032b3892af0c2adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126344304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aef0003a941f9ed6335047bc2741dd2c754246e44b792596444ba505425924b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06b3967b4e642b2d6cb98ddda55dabc4993a3899194dfb50645801f28a2de4d`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.8 MB (18843467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e167d9a57b137b11ef1469f2536ba9c09315dd6e1858686fed99b317c474b`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.1 MB (18112380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746625955b5ebca8aee1d3e40c90c535484d1d6e5dcb2f3af36d50293db19d9b`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778bb8e57da23192256e4be8f68202f6916ae3d97cd410afd26a12c5157d2351`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f6729763aa7494d8f2673d92eaee47a0d1ff164b4022dad21403edbb87ac5`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143d81c732b89ee68c6854c26f60e4bd650052ccaa846e89b879dfd55f47d1e`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 7.0 MB (7041332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70697f77c3da37666380be4a8d5152894d73539601f5b1d05f7f6dfecbafdf40`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 89.1 KB (89095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462068e1d900fc5901c6341ff059c1d41259179a3231131a8a94fd3eaf64df4c`  
		Last Modified: Tue, 21 Jan 2025 21:07:26 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f718a2a569cddb414e88527a1c82a5249ef00ed13d6d969d03fd6fe947be4b0`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877f61b5788c314f1cac1b07c0313c5527bc575bcd4d8b3272428ee623f3b274`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23f9c5dc2c1283e409e70ca0d2b4a332c5801dc25dc5843d1757ab106ed8c0`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b1f9791b335c7b2bb6a757c468f291e693c2ccdf3877d6824d897eb61a4d54df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520c66be7ff520149482f170959560d0ba42369cac8764a5c7a7f77c5508bca8`

```dockerfile
```

-	Layers:
	-	`sha256:eeb9d59564585bc42c45673ed7070fabc5908a173de9834f878eda77da97e602`  
		Last Modified: Tue, 21 Jan 2025 21:07:25 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:f8f084af66dcc16af366577ae5c690b03d7cfac9e61cd0f96b8059a0fb45b973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124682037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540a5c12b45b516c76d8ea89c3597f0793e3798019bddf32d002d8f5ea5c33a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ac6636f9483ab54616b64903f8ba8d2cccee9440eb895c78d56ace8d3e4f96`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 6.4 MB (6367540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5348b12a83f89cbde850839c9f9cbbcb324c91ba1d7f5c1a142a6b282380fa8`  
		Last Modified: Tue, 21 Jan 2025 21:07:28 GMT  
		Size: 85.2 KB (85240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eec605d713ebdd1bfff3c3503cc918cb50f85ece729d9770a8209d44099ddb7`  
		Last Modified: Tue, 21 Jan 2025 21:07:29 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf469db7797818d99b9e99e927b899189f5993e54bb858b340b9eb4e3900a771`  
		Last Modified: Tue, 21 Jan 2025 21:07:31 GMT  
		Size: 54.0 MB (54047072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8360a16ab6657a3443418100cf468a24ee74c8c7e9eaa7582055fe8081c0140`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25fdd4000a14fc00def0dfdc4c82344e1c846243be32bb60c28b8d110b744d`  
		Last Modified: Tue, 21 Jan 2025 21:07:30 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:3c7af3642f4779bc4148276b9902201860a53549bb11720b590ae5017cba85bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbf80603931802b71715d79b520e20f5ed851543f67792da506a4a5b901f599`

```dockerfile
```

-	Layers:
	-	`sha256:b8f59cb6e5ce03d8cfe1900ab25b26a4611e555e10cd4f04345b772825949593`  
		Last Modified: Tue, 21 Jan 2025 21:07:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:97085805b3bcab3e576f5f96c8ee56e3f566746cb735898873d28caaa7871120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72ef41ef6ce6aba1ea0dfb67400cb2fb10157d65e30432393cec3061a60a00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
VOLUME [/var/lib/docker]
# Wed, 22 Jan 2025 18:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1580304ef1db2d9a8fc9c312a3c7d03077b3f4c8f666eb7e8e39652316ef32`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 7.0 MB (6981853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6cc9f41f9170dd177445ed39998d3f2ba3ebac2ff316c3e9c099657326786`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44f0d1bc4efa5005bb5fd76a7db1d2f29880bb7990da98f8960bec36cc50ad`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178470bb2ba3e8b05f3e3bfe2ed21d53d6a8c45788e6bc0d1588def92e13af3`  
		Last Modified: Wed, 22 Jan 2025 23:36:42 GMT  
		Size: 54.0 MB (53950864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174d014cc2baaa28f311dad774a0021096d4e6534de71fac78a727f3ee63b6c`  
		Last Modified: Wed, 22 Jan 2025 23:36:40 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f9b8afbfff0029f00733e903a52813498da6ec1179896a26440d820e36328e`  
		Last Modified: Wed, 22 Jan 2025 23:36:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b745d1b21ae1904bdb5043827ecc9ff47b091dcfd13162e233c3449ef0a27a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cfa4a5cbcec5eb4090a80cb0f552ad8df7db4366164566e9b73be55014281`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea4339accf695ac1828942d5af09b5bc0a7f16024f2844b47f58ecd46f357`  
		Last Modified: Wed, 22 Jan 2025 23:36:39 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:b6f8b0d57df4a2696419a5762e577d335b8045344e3955e8f4dbe161e18af19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Thu, 23 Jan 2025 01:33:30 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:5c1a568071d5c38211f0f2ab29165658baa270218a50280ea14a48e551fdb8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323144969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7fa5f72ee91f71047e0cae9811ca6f53ba1a60cdb312db0a9d0345798a4187`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 01:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:28:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:28:53 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:28:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:29:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:29:14 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:29:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed09903d475f8bbfa96b9ead8ead4f2a39d0f719b474586e24a4a58b9470345e`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52dc955ea9bebcaa9ed296818141638ea1aacbed9fdba231dc54b2980b65a5c`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 361.5 KB (361541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a2af8cdcfc4a587bf767381b48afc6c8a51de1f15d8bc0b58ab40283a5f4b`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03fc4d8fe06a92147d6a07ecb5da93751eb8bba0ddcf071c2c3cae0a21b87e3`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb589666dc5302c33e2bd3103275dce7cc6d806c1f7941c8b7d21cfb86111fdc`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 19.1 MB (19134262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a47ad75b95b47fedf86cc1b64b2ee05f4d918b17abd048778f49815048d7510`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38a2eb0cc0556e4da418dfa0ee2cdc500a1f6939268795cfc7257456825f41`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f4b5f8bb28da0ae8bbf98a59430a7a7bc9c34fd58f375b55d628b8b87ab0b7`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c4b941c28c51cd43369ba6156390bdf5fb913aeb0f27ac099875fe7524cae4`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 21.1 MB (21112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d65a4d2b1bb37dc218ab758d1ceee791d50caec34bb6831847c4a8160c67a`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e41bf06ac3da01d5d8fad12e4accd484fedf4eba4a806a136587de0f9b1cda`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ae2d6a0e330b4f2d8f8b93d611370649ad1f85767b559b921a5c1ee27b5bd`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8b1dd36f2eb10913aef8028fb60fb8cd6ef11f7e112ee8ffbbe965253d530`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 20.1 MB (20140156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:38bc4d48f3168306d2d648e0af9406d27bb41a6537d46185c81cefb8ebef842d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183020077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3b61b7f9129666ce834144f71d29ff871f27da200bb6cf5e5f7c0aef7c6ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 01:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:35:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:35:13 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:35:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:35:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:35:29 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:35:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:35:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e1f7a6ddd0af874949fad5fb2b18dc713d63a1972a77488e76118dd264f9d6`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33a1f96da749ae14a963290552db28406e792510359e069b46c86dcf63dc44`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 339.2 KB (339235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72e1a49e563e9bd93904b22396c2cd2f02b470a1bde810aa4003c0ef0ab56`  
		Last Modified: Thu, 23 Jan 2025 01:36:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a932c4224a159c091a14b8d1fe2b1c82bd3a605f046e5770a30f20464d41`  
		Last Modified: Thu, 23 Jan 2025 01:35:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60ccc3c7b375c18d01ab1d49ab7bbe737fc195d6d8e69b61742a296795eb775`  
		Last Modified: Thu, 23 Jan 2025 01:36:01 GMT  
		Size: 19.2 MB (19162080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbc1c67f17e5b2e533cc4d4cbf4892631ec102977971247237ed7b91d36994`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4841f280b69012015b175aa6b6f87bc6d793a6e8d36f300ad59f649531a6d1`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d47b4005db434e43608202c5acadac1e39ac41c7da57dc0ed3db8b450198b6f`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ce7b9a878c3aff2e2a97b385f7c75f6043234bb92a724f5f7c060be0032be1`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 21.1 MB (21130564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd9a849c2c7eefd648403d5cd4e04a259de2927c100bc629bbbb132b5f821c3`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5505d56ad65828edc87e543f61694fe4bc77d3be290c27ecf695f8625ba2c415`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce02b8200d83f1b73eeee2e5797bdb4fe5b87497dea1b31c3a655e45cd8d011c`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042952d001e4adcdab5611fa007695ef67a2707230a2be2278cd1fc6cea222a4`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 20.2 MB (20163992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:383bafe0d882dfaee478abe15a862e5a2cbd50cef39a1ca7bfa511fdff4053cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:38bc4d48f3168306d2d648e0af9406d27bb41a6537d46185c81cefb8ebef842d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183020077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3b61b7f9129666ce834144f71d29ff871f27da200bb6cf5e5f7c0aef7c6ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 01:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:35:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:35:13 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:35:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:35:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:35:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:35:29 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:35:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:35:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:35:40 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:35:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e1f7a6ddd0af874949fad5fb2b18dc713d63a1972a77488e76118dd264f9d6`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33a1f96da749ae14a963290552db28406e792510359e069b46c86dcf63dc44`  
		Last Modified: Thu, 23 Jan 2025 01:36:00 GMT  
		Size: 339.2 KB (339235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72e1a49e563e9bd93904b22396c2cd2f02b470a1bde810aa4003c0ef0ab56`  
		Last Modified: Thu, 23 Jan 2025 01:36:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a932c4224a159c091a14b8d1fe2b1c82bd3a605f046e5770a30f20464d41`  
		Last Modified: Thu, 23 Jan 2025 01:35:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60ccc3c7b375c18d01ab1d49ab7bbe737fc195d6d8e69b61742a296795eb775`  
		Last Modified: Thu, 23 Jan 2025 01:36:01 GMT  
		Size: 19.2 MB (19162080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbc1c67f17e5b2e533cc4d4cbf4892631ec102977971247237ed7b91d36994`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4841f280b69012015b175aa6b6f87bc6d793a6e8d36f300ad59f649531a6d1`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d47b4005db434e43608202c5acadac1e39ac41c7da57dc0ed3db8b450198b6f`  
		Last Modified: Thu, 23 Jan 2025 01:35:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ce7b9a878c3aff2e2a97b385f7c75f6043234bb92a724f5f7c060be0032be1`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 21.1 MB (21130564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd9a849c2c7eefd648403d5cd4e04a259de2927c100bc629bbbb132b5f821c3`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5505d56ad65828edc87e543f61694fe4bc77d3be290c27ecf695f8625ba2c415`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce02b8200d83f1b73eeee2e5797bdb4fe5b87497dea1b31c3a655e45cd8d011c`  
		Last Modified: Thu, 23 Jan 2025 01:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042952d001e4adcdab5611fa007695ef67a2707230a2be2278cd1fc6cea222a4`  
		Last Modified: Thu, 23 Jan 2025 01:35:58 GMT  
		Size: 20.2 MB (20163992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c37cf3b88ac15878732da1a35ced92a3889e31d4512d22dac218f03dc9cedb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:5c1a568071d5c38211f0f2ab29165658baa270218a50280ea14a48e551fdb8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323144969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7fa5f72ee91f71047e0cae9811ca6f53ba1a60cdb312db0a9d0345798a4187`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 01:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:28:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:28:53 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:28:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:29:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:12 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:29:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:29:14 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:29:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed09903d475f8bbfa96b9ead8ead4f2a39d0f719b474586e24a4a58b9470345e`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52dc955ea9bebcaa9ed296818141638ea1aacbed9fdba231dc54b2980b65a5c`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 361.5 KB (361541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a2af8cdcfc4a587bf767381b48afc6c8a51de1f15d8bc0b58ab40283a5f4b`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03fc4d8fe06a92147d6a07ecb5da93751eb8bba0ddcf071c2c3cae0a21b87e3`  
		Last Modified: Thu, 23 Jan 2025 01:29:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb589666dc5302c33e2bd3103275dce7cc6d806c1f7941c8b7d21cfb86111fdc`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 19.1 MB (19134262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a47ad75b95b47fedf86cc1b64b2ee05f4d918b17abd048778f49815048d7510`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38a2eb0cc0556e4da418dfa0ee2cdc500a1f6939268795cfc7257456825f41`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f4b5f8bb28da0ae8bbf98a59430a7a7bc9c34fd58f375b55d628b8b87ab0b7`  
		Last Modified: Thu, 23 Jan 2025 01:29:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c4b941c28c51cd43369ba6156390bdf5fb913aeb0f27ac099875fe7524cae4`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 21.1 MB (21112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d65a4d2b1bb37dc218ab758d1ceee791d50caec34bb6831847c4a8160c67a`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e41bf06ac3da01d5d8fad12e4accd484fedf4eba4a806a136587de0f9b1cda`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ae2d6a0e330b4f2d8f8b93d611370649ad1f85767b559b921a5c1ee27b5bd`  
		Last Modified: Thu, 23 Jan 2025 01:29:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8b1dd36f2eb10913aef8028fb60fb8cd6ef11f7e112ee8ffbbe965253d530`  
		Last Modified: Thu, 23 Jan 2025 01:29:46 GMT  
		Size: 20.1 MB (20140156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c68bdfb265f8b44bdcdbd856c52b597a0adc9e70d38d1073c2dcbeb23e26818e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:20e8814de9566c22c879cb2c96356f804d2c92d94f9fe8dda89e8e6d116e7d11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561296529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e125151f9cd80d68e4da70de3efbaa68df16ba9052085473f449e71caf50f68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 01:32:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 01:32:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 23 Jan 2025 01:32:38 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 01:32:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 23 Jan 2025 01:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:32:54 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 01:32:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 23 Jan 2025 01:32:56 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 23 Jan 2025 01:33:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 23 Jan 2025 01:33:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 01:33:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Thu, 23 Jan 2025 01:33:09 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Thu, 23 Jan 2025 01:33:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149956c470fc4542250de56a82ded57ed2f6512565ac59d8c74c18daca3d8e52`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a088cd9046360ec31cb435a7baba5e5264e5d136d38fffb48545323dd2207265`  
		Last Modified: Thu, 23 Jan 2025 01:33:29 GMT  
		Size: 394.1 KB (394142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1d51de51c6181e07a2cf5fc673d6595f574527cc147cf6ec357c319efd67e`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0455135a934d9ce099dbf28b21ae0025f73e190141fee84c373d47058c3b9b`  
		Last Modified: Thu, 23 Jan 2025 01:33:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714343b652340fcdfe10cccb204c9fba1ed7b8a16533c8854ef72f4bc59eaa6`  
		Last Modified: Thu, 23 Jan 2025 01:33:30 GMT  
		Size: 19.2 MB (19211347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ad31e7954869b3bb8d6cac1c7c4b6606803880460eaa54992c181234679ce`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb12258e6beccbeb82a488ccfae50d2fc8974b6d21f4fcb4aab75c383a8765b`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69150cb6a461210c4a66295aff6d5d04cb554b5d6119a4f911f712a463f8cffb`  
		Last Modified: Thu, 23 Jan 2025 01:33:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d50cb251bb21329a2cc318e2f6be612903c51930eadeae4b4791cb7ce1e09b`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 21.2 MB (21187570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccba2502c904bfc96a3679d74f9dfb8cedf0156a5e02280d68fbf0c0e7298cc6`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c9cada410206266628ce2a5007baede68c4a1221cb61800b21b8f1f38f932c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8a3c0c6cb2bf92e57f35c86823d46ea45c33bcd519a173c8d3ef5db98c76c`  
		Last Modified: Thu, 23 Jan 2025 01:33:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd6ff04c1de3614982f9e148e757789570370ca2bcf0447f7c8cb2882d666f`  
		Last Modified: Thu, 23 Jan 2025 01:33:27 GMT  
		Size: 20.2 MB (20214057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
