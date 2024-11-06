<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27.3`](#docker273)
-	[`docker:27.3-cli`](#docker273-cli)
-	[`docker:27.3-dind`](#docker273-dind)
-	[`docker:27.3-dind-rootless`](#docker273-dind-rootless)
-	[`docker:27.3-windowsservercore`](#docker273-windowsservercore)
-	[`docker:27.3-windowsservercore-1809`](#docker273-windowsservercore-1809)
-	[`docker:27.3-windowsservercore-ltsc2022`](#docker273-windowsservercore-ltsc2022)
-	[`docker:27.3.1`](#docker2731)
-	[`docker:27.3.1-alpine3.20`](#docker2731-alpine320)
-	[`docker:27.3.1-cli`](#docker2731-cli)
-	[`docker:27.3.1-cli-alpine3.20`](#docker2731-cli-alpine320)
-	[`docker:27.3.1-dind`](#docker2731-dind)
-	[`docker:27.3.1-dind-alpine3.20`](#docker2731-dind-alpine320)
-	[`docker:27.3.1-dind-rootless`](#docker2731-dind-rootless)
-	[`docker:27.3.1-windowsservercore`](#docker2731-windowsservercore)
-	[`docker:27.3.1-windowsservercore-1809`](#docker2731-windowsservercore-1809)
-	[`docker:27.3.1-windowsservercore-ltsc2022`](#docker2731-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:3486a702666745d124e1cd4452fb54d83789f735de9cedd4069d9d502065f692
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
$ docker pull docker@sha256:f2801be3440b90450aa31e12b2eabc05c25e73121f94a5d586561a98746d1bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67763121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8a61369db9e638cfb70d258507387d7e7e1288e3cf40cf073d741f30f5a9ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:45be58be6dc9dce5fa6181734a506c8901659c7956b3af5bff59692dfa7571c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7d61a68d868262220d2ca3efde40f5b4727014938e45dbd0eaeadac1547fc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd20cd91b5aebf693c5fb38d516f8016562bc6ff4272e1502c5c97af59c81c6`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c95debe39252628ead592962bb624ff131ef6054aee786b9f1166656636c4485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62009875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9eb3dd47ab956b4a4ec0801db472cb508d4ddc4fd91aa947fdb6234651b2185`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ab2a4aebf76b0f25badf4890a867c426814d31ca137a9fb448d549bbb3c39b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9ff21d60f9a42c750a9a43cf64ece7e7baba14a6d24a25306daa18b112d1d1`

```dockerfile
```

-	Layers:
	-	`sha256:381e55a3ea7f67fb99e65834af6a60bd686e1bc4634eb6f20c7bb3cea230a9b6`  
		Last Modified: Tue, 05 Nov 2024 20:59:04 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3742107db033a0ffe2044234a11cabe31f22d7622ed871b2964ce8e0178c03eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c894547a0ed403ca7cc8aeeb96fccf25556de38991be54a3ceb59ddc45d808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:753e957b7506c34733b986aa67bc6d13290df89cf35ac3ad29c58b67b85c8fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b67c22bb984bef0b64a776a355e40b269d6eb6208e0af05f6b97227532756c`

```dockerfile
```

-	Layers:
	-	`sha256:4ed4997071d9da3e39103f4860d9db8374d263ad750704346158e75c0634890f`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:c50376410245bb43ad3eacdf55f60964052381772dc727dd97551089db9dd54d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:931549f5eea3dd68fd542859b64fb124fba866c0935bf952e2cee1cdeacc56e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157010478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2163156d4eccbbe3ebde0e409d9f391d6a80f49abf280f4dcb0b12a8be49f14d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1915f5357c740b5e30b173b94feadf4f5c4bfa27463a2b893e4971cdeb8b9a25`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 981.6 KB (981575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b82f9e6a4ccd59a964c0ad3bb6f14a3f31c926b92dd1686bca3426b508cf47`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec29b2dcecb039549c2b3da115f0a116037f1dd081d4224fe1bd3b458efd7d8`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5557647bff09cea8382ac9f431563bf4fa483b49d5add2535e05d9de95349d`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 21.3 MB (21303256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f67360ee3cc924fc4f78c23f3ced5cddff5b28ccfdb687c2da38b40c959a629`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:58e48442030c8f68789f319229822f6aa645e2d01e39d0f790f6282777ba8015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d48af5bb798a4de5abbb3d6585a71f81cb6b3e297b3979dccb7bb68a5e1cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5df176f3fc75b7957fc7c42830483a0841f5693d66035e3c913d944842ad2ba9`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c440a28534d6544b5558dd0704056b6fd9e0f0c5a62be916c49d3cd1f567cb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151567593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d526e74b8806132257687769680ea4729adb42efab11e5f5f4a1eade77d5e1a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c6209f8ece05c0310870aae2e391cf1c0f536677211222057496b38634016`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 1.0 MB (1023839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed16a9f9298720d2949a1bedaa297a4509064eb0a71967f5fc7a326c832158`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b228cbef45601bbc062075754c4462e987a42cce08a01c6bbf26d8cee7adcf0b`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142e9cff7aec27e6a409a8483598d0eca5f28d44a830503ac9239ca69d12eb76`  
		Last Modified: Tue, 05 Nov 2024 21:47:37 GMT  
		Size: 23.2 MB (23155434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9ed5aee51877fa17b27761b121944116006477bc8cc5ee5376ca8494b1432e`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:df316d394f2282f93ca50a5b82ccdceb292c9ee96ddde7cc47e0e02210e5a700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaef0858e11a6f981140de9773b1b1d92ca183ae0b20f88dc053e533dc3413f5`

```dockerfile
```

-	Layers:
	-	`sha256:3e2b1bb9f6b7e9935d65d654d0d0f03dae4afb41cdab8cf1017b4f388f800f33`  
		Last Modified: Tue, 05 Nov 2024 21:47:34 GMT  
		Size: 30.8 KB (30823 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:cd28bf3a2e7baf7870db5297557509e5f2b6d0b3606056da14b8ec1fa7a63f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:53d0f82df0671a80bac71813cd6239f2c6c24be10aad68ee6b51b935ff629e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:832a0973a728b261599f8aad5ef361bfd16999d86ecf9ed3e206aff94e57af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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

### `docker:27.3` - linux; amd64

```console
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-cli`

```console
$ docker pull docker@sha256:3486a702666745d124e1cd4452fb54d83789f735de9cedd4069d9d502065f692
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

### `docker:27.3-cli` - linux; amd64

```console
$ docker pull docker@sha256:f2801be3440b90450aa31e12b2eabc05c25e73121f94a5d586561a98746d1bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67763121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8a61369db9e638cfb70d258507387d7e7e1288e3cf40cf073d741f30f5a9ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:45be58be6dc9dce5fa6181734a506c8901659c7956b3af5bff59692dfa7571c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7d61a68d868262220d2ca3efde40f5b4727014938e45dbd0eaeadac1547fc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd20cd91b5aebf693c5fb38d516f8016562bc6ff4272e1502c5c97af59c81c6`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c95debe39252628ead592962bb624ff131ef6054aee786b9f1166656636c4485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62009875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9eb3dd47ab956b4a4ec0801db472cb508d4ddc4fd91aa947fdb6234651b2185`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ab2a4aebf76b0f25badf4890a867c426814d31ca137a9fb448d549bbb3c39b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9ff21d60f9a42c750a9a43cf64ece7e7baba14a6d24a25306daa18b112d1d1`

```dockerfile
```

-	Layers:
	-	`sha256:381e55a3ea7f67fb99e65834af6a60bd686e1bc4634eb6f20c7bb3cea230a9b6`  
		Last Modified: Tue, 05 Nov 2024 20:59:04 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3742107db033a0ffe2044234a11cabe31f22d7622ed871b2964ce8e0178c03eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c894547a0ed403ca7cc8aeeb96fccf25556de38991be54a3ceb59ddc45d808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:753e957b7506c34733b986aa67bc6d13290df89cf35ac3ad29c58b67b85c8fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b67c22bb984bef0b64a776a355e40b269d6eb6208e0af05f6b97227532756c`

```dockerfile
```

-	Layers:
	-	`sha256:4ed4997071d9da3e39103f4860d9db8374d263ad750704346158e75c0634890f`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-dind`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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

### `docker:27.3-dind` - linux; amd64

```console
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-dind-rootless`

```console
$ docker pull docker@sha256:c50376410245bb43ad3eacdf55f60964052381772dc727dd97551089db9dd54d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:931549f5eea3dd68fd542859b64fb124fba866c0935bf952e2cee1cdeacc56e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157010478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2163156d4eccbbe3ebde0e409d9f391d6a80f49abf280f4dcb0b12a8be49f14d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1915f5357c740b5e30b173b94feadf4f5c4bfa27463a2b893e4971cdeb8b9a25`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 981.6 KB (981575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b82f9e6a4ccd59a964c0ad3bb6f14a3f31c926b92dd1686bca3426b508cf47`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec29b2dcecb039549c2b3da115f0a116037f1dd081d4224fe1bd3b458efd7d8`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5557647bff09cea8382ac9f431563bf4fa483b49d5add2535e05d9de95349d`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 21.3 MB (21303256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f67360ee3cc924fc4f78c23f3ced5cddff5b28ccfdb687c2da38b40c959a629`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:58e48442030c8f68789f319229822f6aa645e2d01e39d0f790f6282777ba8015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d48af5bb798a4de5abbb3d6585a71f81cb6b3e297b3979dccb7bb68a5e1cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5df176f3fc75b7957fc7c42830483a0841f5693d66035e3c913d944842ad2ba9`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c440a28534d6544b5558dd0704056b6fd9e0f0c5a62be916c49d3cd1f567cb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151567593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d526e74b8806132257687769680ea4729adb42efab11e5f5f4a1eade77d5e1a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c6209f8ece05c0310870aae2e391cf1c0f536677211222057496b38634016`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 1.0 MB (1023839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed16a9f9298720d2949a1bedaa297a4509064eb0a71967f5fc7a326c832158`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b228cbef45601bbc062075754c4462e987a42cce08a01c6bbf26d8cee7adcf0b`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142e9cff7aec27e6a409a8483598d0eca5f28d44a830503ac9239ca69d12eb76`  
		Last Modified: Tue, 05 Nov 2024 21:47:37 GMT  
		Size: 23.2 MB (23155434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9ed5aee51877fa17b27761b121944116006477bc8cc5ee5376ca8494b1432e`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:df316d394f2282f93ca50a5b82ccdceb292c9ee96ddde7cc47e0e02210e5a700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaef0858e11a6f981140de9773b1b1d92ca183ae0b20f88dc053e533dc3413f5`

```dockerfile
```

-	Layers:
	-	`sha256:3e2b1bb9f6b7e9935d65d654d0d0f03dae4afb41cdab8cf1017b4f388f800f33`  
		Last Modified: Tue, 05 Nov 2024 21:47:34 GMT  
		Size: 30.8 KB (30823 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-windowsservercore`

```console
$ docker pull docker@sha256:cd28bf3a2e7baf7870db5297557509e5f2b6d0b3606056da14b8ec1fa7a63f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-1809`

```console
$ docker pull docker@sha256:53d0f82df0671a80bac71813cd6239f2c6c24be10aad68ee6b51b935ff629e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:832a0973a728b261599f8aad5ef361bfd16999d86ecf9ed3e206aff94e57af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27.3-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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

### `docker:27.3.1` - linux; amd64

```console
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-alpine3.20`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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

### `docker:27.3.1-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-cli`

```console
$ docker pull docker@sha256:3486a702666745d124e1cd4452fb54d83789f735de9cedd4069d9d502065f692
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

### `docker:27.3.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:f2801be3440b90450aa31e12b2eabc05c25e73121f94a5d586561a98746d1bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67763121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8a61369db9e638cfb70d258507387d7e7e1288e3cf40cf073d741f30f5a9ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:45be58be6dc9dce5fa6181734a506c8901659c7956b3af5bff59692dfa7571c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7d61a68d868262220d2ca3efde40f5b4727014938e45dbd0eaeadac1547fc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd20cd91b5aebf693c5fb38d516f8016562bc6ff4272e1502c5c97af59c81c6`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c95debe39252628ead592962bb624ff131ef6054aee786b9f1166656636c4485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62009875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9eb3dd47ab956b4a4ec0801db472cb508d4ddc4fd91aa947fdb6234651b2185`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ab2a4aebf76b0f25badf4890a867c426814d31ca137a9fb448d549bbb3c39b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9ff21d60f9a42c750a9a43cf64ece7e7baba14a6d24a25306daa18b112d1d1`

```dockerfile
```

-	Layers:
	-	`sha256:381e55a3ea7f67fb99e65834af6a60bd686e1bc4634eb6f20c7bb3cea230a9b6`  
		Last Modified: Tue, 05 Nov 2024 20:59:04 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3742107db033a0ffe2044234a11cabe31f22d7622ed871b2964ce8e0178c03eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c894547a0ed403ca7cc8aeeb96fccf25556de38991be54a3ceb59ddc45d808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:753e957b7506c34733b986aa67bc6d13290df89cf35ac3ad29c58b67b85c8fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b67c22bb984bef0b64a776a355e40b269d6eb6208e0af05f6b97227532756c`

```dockerfile
```

-	Layers:
	-	`sha256:4ed4997071d9da3e39103f4860d9db8374d263ad750704346158e75c0634890f`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-cli-alpine3.20`

```console
$ docker pull docker@sha256:3486a702666745d124e1cd4452fb54d83789f735de9cedd4069d9d502065f692
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

### `docker:27.3.1-cli-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:f2801be3440b90450aa31e12b2eabc05c25e73121f94a5d586561a98746d1bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67763121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8a61369db9e638cfb70d258507387d7e7e1288e3cf40cf073d741f30f5a9ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:45be58be6dc9dce5fa6181734a506c8901659c7956b3af5bff59692dfa7571c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7d61a68d868262220d2ca3efde40f5b4727014938e45dbd0eaeadac1547fc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd20cd91b5aebf693c5fb38d516f8016562bc6ff4272e1502c5c97af59c81c6`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:c95debe39252628ead592962bb624ff131ef6054aee786b9f1166656636c4485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62009875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9eb3dd47ab956b4a4ec0801db472cb508d4ddc4fd91aa947fdb6234651b2185`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:ab2a4aebf76b0f25badf4890a867c426814d31ca137a9fb448d549bbb3c39b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9ff21d60f9a42c750a9a43cf64ece7e7baba14a6d24a25306daa18b112d1d1`

```dockerfile
```

-	Layers:
	-	`sha256:381e55a3ea7f67fb99e65834af6a60bd686e1bc4634eb6f20c7bb3cea230a9b6`  
		Last Modified: Tue, 05 Nov 2024 20:59:04 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3742107db033a0ffe2044234a11cabe31f22d7622ed871b2964ce8e0178c03eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c894547a0ed403ca7cc8aeeb96fccf25556de38991be54a3ceb59ddc45d808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:753e957b7506c34733b986aa67bc6d13290df89cf35ac3ad29c58b67b85c8fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b67c22bb984bef0b64a776a355e40b269d6eb6208e0af05f6b97227532756c`

```dockerfile
```

-	Layers:
	-	`sha256:4ed4997071d9da3e39103f4860d9db8374d263ad750704346158e75c0634890f`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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

### `docker:27.3.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind-alpine3.20`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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

### `docker:27.3.1-dind-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind-rootless`

```console
$ docker pull docker@sha256:c50376410245bb43ad3eacdf55f60964052381772dc727dd97551089db9dd54d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:931549f5eea3dd68fd542859b64fb124fba866c0935bf952e2cee1cdeacc56e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157010478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2163156d4eccbbe3ebde0e409d9f391d6a80f49abf280f4dcb0b12a8be49f14d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1915f5357c740b5e30b173b94feadf4f5c4bfa27463a2b893e4971cdeb8b9a25`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 981.6 KB (981575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b82f9e6a4ccd59a964c0ad3bb6f14a3f31c926b92dd1686bca3426b508cf47`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec29b2dcecb039549c2b3da115f0a116037f1dd081d4224fe1bd3b458efd7d8`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5557647bff09cea8382ac9f431563bf4fa483b49d5add2535e05d9de95349d`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 21.3 MB (21303256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f67360ee3cc924fc4f78c23f3ced5cddff5b28ccfdb687c2da38b40c959a629`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:58e48442030c8f68789f319229822f6aa645e2d01e39d0f790f6282777ba8015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d48af5bb798a4de5abbb3d6585a71f81cb6b3e297b3979dccb7bb68a5e1cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5df176f3fc75b7957fc7c42830483a0841f5693d66035e3c913d944842ad2ba9`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c440a28534d6544b5558dd0704056b6fd9e0f0c5a62be916c49d3cd1f567cb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151567593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d526e74b8806132257687769680ea4729adb42efab11e5f5f4a1eade77d5e1a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c6209f8ece05c0310870aae2e391cf1c0f536677211222057496b38634016`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 1.0 MB (1023839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed16a9f9298720d2949a1bedaa297a4509064eb0a71967f5fc7a326c832158`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b228cbef45601bbc062075754c4462e987a42cce08a01c6bbf26d8cee7adcf0b`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142e9cff7aec27e6a409a8483598d0eca5f28d44a830503ac9239ca69d12eb76`  
		Last Modified: Tue, 05 Nov 2024 21:47:37 GMT  
		Size: 23.2 MB (23155434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9ed5aee51877fa17b27761b121944116006477bc8cc5ee5376ca8494b1432e`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:df316d394f2282f93ca50a5b82ccdceb292c9ee96ddde7cc47e0e02210e5a700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaef0858e11a6f981140de9773b1b1d92ca183ae0b20f88dc053e533dc3413f5`

```dockerfile
```

-	Layers:
	-	`sha256:3e2b1bb9f6b7e9935d65d654d0d0f03dae4afb41cdab8cf1017b4f388f800f33`  
		Last Modified: Tue, 05 Nov 2024 21:47:34 GMT  
		Size: 30.8 KB (30823 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-windowsservercore`

```console
$ docker pull docker@sha256:cd28bf3a2e7baf7870db5297557509e5f2b6d0b3606056da14b8ec1fa7a63f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3.1-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3.1-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:53d0f82df0671a80bac71813cd6239f2c6c24be10aad68ee6b51b935ff629e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3.1-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:832a0973a728b261599f8aad5ef361bfd16999d86ecf9ed3e206aff94e57af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27.3.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:3486a702666745d124e1cd4452fb54d83789f735de9cedd4069d9d502065f692
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
$ docker pull docker@sha256:f2801be3440b90450aa31e12b2eabc05c25e73121f94a5d586561a98746d1bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67763121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8a61369db9e638cfb70d258507387d7e7e1288e3cf40cf073d741f30f5a9ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:45be58be6dc9dce5fa6181734a506c8901659c7956b3af5bff59692dfa7571c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7d61a68d868262220d2ca3efde40f5b4727014938e45dbd0eaeadac1547fc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd20cd91b5aebf693c5fb38d516f8016562bc6ff4272e1502c5c97af59c81c6`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c95debe39252628ead592962bb624ff131ef6054aee786b9f1166656636c4485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62009875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9eb3dd47ab956b4a4ec0801db472cb508d4ddc4fd91aa947fdb6234651b2185`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:ab2a4aebf76b0f25badf4890a867c426814d31ca137a9fb448d549bbb3c39b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9ff21d60f9a42c750a9a43cf64ece7e7baba14a6d24a25306daa18b112d1d1`

```dockerfile
```

-	Layers:
	-	`sha256:381e55a3ea7f67fb99e65834af6a60bd686e1bc4634eb6f20c7bb3cea230a9b6`  
		Last Modified: Tue, 05 Nov 2024 20:59:04 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3742107db033a0ffe2044234a11cabe31f22d7622ed871b2964ce8e0178c03eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c894547a0ed403ca7cc8aeeb96fccf25556de38991be54a3ceb59ddc45d808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:753e957b7506c34733b986aa67bc6d13290df89cf35ac3ad29c58b67b85c8fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b67c22bb984bef0b64a776a355e40b269d6eb6208e0af05f6b97227532756c`

```dockerfile
```

-	Layers:
	-	`sha256:4ed4997071d9da3e39103f4860d9db8374d263ad750704346158e75c0634890f`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:c50376410245bb43ad3eacdf55f60964052381772dc727dd97551089db9dd54d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:931549f5eea3dd68fd542859b64fb124fba866c0935bf952e2cee1cdeacc56e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157010478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2163156d4eccbbe3ebde0e409d9f391d6a80f49abf280f4dcb0b12a8be49f14d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1915f5357c740b5e30b173b94feadf4f5c4bfa27463a2b893e4971cdeb8b9a25`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 981.6 KB (981575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b82f9e6a4ccd59a964c0ad3bb6f14a3f31c926b92dd1686bca3426b508cf47`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec29b2dcecb039549c2b3da115f0a116037f1dd081d4224fe1bd3b458efd7d8`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5557647bff09cea8382ac9f431563bf4fa483b49d5add2535e05d9de95349d`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 21.3 MB (21303256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f67360ee3cc924fc4f78c23f3ced5cddff5b28ccfdb687c2da38b40c959a629`  
		Last Modified: Tue, 05 Nov 2024 21:47:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:58e48442030c8f68789f319229822f6aa645e2d01e39d0f790f6282777ba8015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d48af5bb798a4de5abbb3d6585a71f81cb6b3e297b3979dccb7bb68a5e1cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5df176f3fc75b7957fc7c42830483a0841f5693d66035e3c913d944842ad2ba9`  
		Last Modified: Tue, 05 Nov 2024 21:47:48 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c440a28534d6544b5558dd0704056b6fd9e0f0c5a62be916c49d3cd1f567cb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151567593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d526e74b8806132257687769680ea4729adb42efab11e5f5f4a1eade77d5e1a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c6209f8ece05c0310870aae2e391cf1c0f536677211222057496b38634016`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 1.0 MB (1023839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed16a9f9298720d2949a1bedaa297a4509064eb0a71967f5fc7a326c832158`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b228cbef45601bbc062075754c4462e987a42cce08a01c6bbf26d8cee7adcf0b`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142e9cff7aec27e6a409a8483598d0eca5f28d44a830503ac9239ca69d12eb76`  
		Last Modified: Tue, 05 Nov 2024 21:47:37 GMT  
		Size: 23.2 MB (23155434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9ed5aee51877fa17b27761b121944116006477bc8cc5ee5376ca8494b1432e`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:df316d394f2282f93ca50a5b82ccdceb292c9ee96ddde7cc47e0e02210e5a700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaef0858e11a6f981140de9773b1b1d92ca183ae0b20f88dc053e533dc3413f5`

```dockerfile
```

-	Layers:
	-	`sha256:3e2b1bb9f6b7e9935d65d654d0d0f03dae4afb41cdab8cf1017b4f388f800f33`  
		Last Modified: Tue, 05 Nov 2024 21:47:34 GMT  
		Size: 30.8 KB (30823 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:ccfd877fe10a2fe0cdb1f35c43aba2fed90007dbf7e0678b1951297c72296e8d
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
$ docker pull docker@sha256:150d3ad8e0ed244f75fcda05f562564ea36dd647c06200844b289d47b71700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134724297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83ff20bb3233a5e116cabf3da580b24d9448a15677b33873ea81f588744e5d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9668ef49501e126169e5379bfbc389cd74b79519e773c02c84ae4c01a05e5165`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 9.1 MB (9067221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60245f8eda9ddc6df96dd1ae016896797385567fa72c9f0d2e2841898a9cb0d0`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5380b581abe9ec0b6b466ff93e43a409bc09505ec8cb8cc1a55fdb42d3208f`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612c2c8e9c4d0dc4bd114da4136ed4e5fcff22cf7ec371a7c142dd07ee0fd43`  
		Last Modified: Tue, 05 Nov 2024 21:10:47 GMT  
		Size: 57.8 MB (57798933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b1d76e3e14bffae749427d46f55e486b1524d59a2cd7c2a9949b079f27269`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913bd2f121075ab50b395c2a12635e5590fa0968e8fea65e7eb0795329cdb01`  
		Last Modified: Tue, 05 Nov 2024 21:10:45 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:9ee20d8d518d973782c42591262b768f86b8d236335a95892a8ac16bac5e76b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546331c7688dbd77580ffccffb0e6f8b685ad8130f5404f7ba5da99892e9594`

```dockerfile
```

-	Layers:
	-	`sha256:aa20e297b192218af20908afa11370d64335859a8f6b0e8f63b8781ae403b743`  
		Last Modified: Tue, 05 Nov 2024 21:10:44 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:30ddbe040b76ffb076fb85689a43572dcdc4d299f53dedfb0f9de8f336f91890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125650353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0bccc0a769fbdd3df1c7f8bbfff6f9d1728dcbcc225d577a504bb73c86288`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f394785e3adbf395eea43391caee3a7f536bdd3145c459c075ea01cd439c0`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 9.1 MB (9060233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277509186937d1eb1cf33c6f0eeac187c26368d2f51bad4de29d22dd41bb89f`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb28214e5274cdb29501586e3cac2802207a89e872e0b0ddb85cdf05a975433`  
		Last Modified: Tue, 05 Nov 2024 21:10:28 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd18425295122083f37388cb080085cde966e375ea3b377042df60ed596e3c`  
		Last Modified: Tue, 05 Nov 2024 21:10:31 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03b314ff4e92813ca26339b639b8de511d84c893b09519d77ecbbe6e4cc90c`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16483f3c4f4698f72b7e7e164822529f79f354c06c9dc8223e44068d5bb135`  
		Last Modified: Tue, 05 Nov 2024 21:10:29 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:3543b5f888f56300d4317cfa98e26b0bfa2bf453afc069fe914a3a1ac5611ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ab6c74d85e009e23f94a815a12da1c418d734baaf454aea2b925973b33350`

```dockerfile
```

-	Layers:
	-	`sha256:2416fbb0401d15268b9636a3ee993f8c9dc2878e9f8aad025e553148483bfdad`  
		Last Modified: Tue, 05 Nov 2024 21:10:27 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:22f4753bf029701ccacc236a28be692a2b58d315a70012f653cf22035a435ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406fd7108d508577ce75c8c3113059ca84a3925b5b7f48faa12e1c99d7ad2774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cced3a7a1624d6288ab4b98fb63f101598f4973b79c1dcb071492a4fe1a73146`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 8.2 MB (8228337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbffffe358c9daca7c1e0eb67084ab671d9c616d718ae18e2a501c56f835cc`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 84.5 KB (84508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f62c45f00f57f624dbba3029d6d5c2042a92f7423a9cfb0cc719371b6349c`  
		Last Modified: Tue, 05 Nov 2024 21:45:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e2fcfc815ed27291728a6e0a082f3f4d2958e10e4801b5f5c236cb25ef67`  
		Last Modified: Tue, 05 Nov 2024 21:45:35 GMT  
		Size: 53.5 MB (53511025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13837a619258d404b268e260708348ecf6995bf201bd80910041bf8e45c07e`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f26963037e2055dc2ec1c7c8bd30b0d3e6892d4d345da7eee4e35ca546ec6`  
		Last Modified: Tue, 05 Nov 2024 21:45:34 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:68f9bb6d162ccad028f29373aa15a90a30e5e3a62f834140742117da19f34a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a2ae24870fab7d1dea947491f0387c1c4f78d121a41db7d151e45e4023905`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9e516fa617155bd65bfe0fb5009574986fec8f79b187e463ba2655cee8bb5`  
		Last Modified: Tue, 05 Nov 2024 21:45:32 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0d46714e096176d595c73f3bd79f7b83c249cc0cede8b91905c5c5fafefc5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54088cb3657dc3fc1e85355f132de032250fda71eb831c69452303349925ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:d4cf3f2b35418665605fcddf547ad21eba64c1e83326ed01e54c85acffbc5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3771f2e62e589e47d53e72589b3226cb03b08863cd1474de6173ed71decba9`

```dockerfile
```

-	Layers:
	-	`sha256:53a22b23dd653c3ab5f91cd93ea6240bc5922907400936dd70a7783e6b71dc12`  
		Last Modified: Tue, 05 Nov 2024 21:10:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:cd28bf3a2e7baf7870db5297557509e5f2b6d0b3606056da14b8ec1fa7a63f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:53d0f82df0671a80bac71813cd6239f2c6c24be10aad68ee6b51b935ff629e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:832a0973a728b261599f8aad5ef361bfd16999d86ecf9ed3e206aff94e57af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
