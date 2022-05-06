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
-	[`docker:20.10.15`](#docker201015)
-	[`docker:20.10.15-alpine3.15`](#docker201015-alpine315)
-	[`docker:20.10.15-dind`](#docker201015-dind)
-	[`docker:20.10.15-dind-alpine3.15`](#docker201015-dind-alpine315)
-	[`docker:20.10.15-dind-rootless`](#docker201015-dind-rootless)
-	[`docker:20.10.15-git`](#docker201015-git)
-	[`docker:20.10.15-windowsservercore`](#docker201015-windowsservercore)
-	[`docker:20.10.15-windowsservercore-1809`](#docker201015-windowsservercore-1809)
-	[`docker:20.10.15-windowsservercore-ltsc2022`](#docker201015-windowsservercore-ltsc2022)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:20`

```console
$ docker pull docker@sha256:ae371e93d152b87afd483252230fe4d9a4fb860d22fbfd952cec9d9890024b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:01b5f40cce1c35af66084493234610a03024efa5ed68376738d28348363a4692
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69397588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7417809fdb730b60c1b903077030aacc708677cdf02f2416ce413f38e81ec7e0`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7896b5013b29f7939347c46f6f4167286179e35d39defa227bde90ede9b8fb14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64630644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4276b804610ccca519b2419f29c4d8b08a9fe66221dfccb94342683a2f8a8407`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:56f24b157d2335f82fb3b2b22a0bacfe8c4bf3aacc273c806e4d53bbb1255a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:dd3584c00ebb822729dd5d2902e3a579ca87b9590637b5175035c1b05ea2fec0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76137359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a072474332af3e4cf06e349685c4cea8f9e631f0c5cab5b582f3a3ab4cff9b6a`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:02:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Apr 2022 11:02:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:02:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Apr 2022 11:02:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Apr 2022 11:02:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:57 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Apr 2022 11:02:57 GMT
EXPOSE 2375 2376
# Tue, 05 Apr 2022 11:02:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:57 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0af8a24b3d99f5d1b97b69005e6e5e973fd76878eb63382937c166cdf5441e`  
		Last Modified: Tue, 05 Apr 2022 11:04:16 GMT  
		Size: 6.7 MB (6734743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c69def9f2284d6ca51f913d19f45240f7051c275501a791efcbf2390a18704`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2998284497aa95875ef53929de1b46642eec185be6f5dd1a1e772dbce1761102`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67900e1c727f6291a49060673983d9297ce9a47b8e599f10fb276e8ff7973f4f`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 2.7 KB (2748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:333ea2510abe899d7c9f57fbd47d94b4300e46ea1b9972beb14aa0c5867bba13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62dcf8507f3db88fb2e57abaac240a09ea1c7157da93e46836b1d297b7f47a0`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 06 May 2022 00:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 06 May 2022 00:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 06 May 2022 00:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:57 GMT
VOLUME [/var/lib/docker]
# Fri, 06 May 2022 00:39:58 GMT
EXPOSE 2375 2376
# Fri, 06 May 2022 00:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 06 May 2022 00:40:00 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc82fabc8945c86cefb751ae77c8dd196e1ae4c73a5aee9cce65621245b47ae`  
		Last Modified: Fri, 06 May 2022 00:41:35 GMT  
		Size: 6.6 MB (6616060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3820c41861a9c3a37250697cb7e7fdf4e4cc80f0bd9c178d745f027a8a0d131d`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2535fcfc181880522bf4850c1225697df6558a460f38463f088d913c7e12a`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955231fc6b6d87f1db4f6969d0124c7c4128ae1b6eb86f1a6ccacf5d45ecaa3`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:d8fb0f5505924b4e7c520e9e1115d58be5fd6e752d1ae1e0f22dd76c758b2a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d1a3e15aeecebf41c8d9b00747ed033cd946c48645af94d9ee4e1c80ade2bb6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96432886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deda3d6ded5613af44013e788c53e5a0d7e86079e756c6b9014b1b4e7f8a73a9`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:02:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Apr 2022 11:02:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:02:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Apr 2022 11:02:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Apr 2022 11:02:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:57 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Apr 2022 11:02:57 GMT
EXPOSE 2375 2376
# Tue, 05 Apr 2022 11:02:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:57 GMT
CMD []
# Tue, 05 Apr 2022 11:03:01 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Apr 2022 11:03:02 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Apr 2022 11:03:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:03:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Apr 2022 11:03:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Apr 2022 11:03:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Apr 2022 11:03:19 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0af8a24b3d99f5d1b97b69005e6e5e973fd76878eb63382937c166cdf5441e`  
		Last Modified: Tue, 05 Apr 2022 11:04:16 GMT  
		Size: 6.7 MB (6734743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c69def9f2284d6ca51f913d19f45240f7051c275501a791efcbf2390a18704`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2998284497aa95875ef53929de1b46642eec185be6f5dd1a1e772dbce1761102`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67900e1c727f6291a49060673983d9297ce9a47b8e599f10fb276e8ff7973f4f`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 2.7 KB (2748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b588ce9e8fbc77fa67055ed6052e4298508b1fb1b243a0c235fe33418ebaf1c5`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 1.2 MB (1161981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1b74acd02dbc4e96821b38c1e1c58a37727ed03f82437cab1656c15e1d5b16`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b219f357717a1ca5ecae5a8f6141cb714f5782dc31f2ceaa63c7da45c89a42`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e307cac3961eec1242ccb911c3fb275f1287855f424c45c1d79e7edb756a4b89`  
		Last Modified: Tue, 05 Apr 2022 11:04:46 GMT  
		Size: 19.1 MB (19131830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11dca8585ce11aea5a2421a5b4d5d811c7ac4669e739d034620f7f2a7ef23c3`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f87b7f70c9a48c367e5927e328e1b315ec801cc2bde914c380eb220e697eea8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93609717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36974783d1fa9b40e54da0c7835c50e25ec6ba9dd36ece5f4676eaed997cf099`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 06 May 2022 00:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 06 May 2022 00:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 06 May 2022 00:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:57 GMT
VOLUME [/var/lib/docker]
# Fri, 06 May 2022 00:39:58 GMT
EXPOSE 2375 2376
# Fri, 06 May 2022 00:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 06 May 2022 00:40:00 GMT
CMD []
# Fri, 06 May 2022 00:40:08 GMT
RUN apk add --no-cache iproute2
# Fri, 06 May 2022 00:40:09 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 06 May 2022 00:40:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 06 May 2022 00:40:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 06 May 2022 00:40:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 06 May 2022 00:40:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 06 May 2022 00:40:16 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc82fabc8945c86cefb751ae77c8dd196e1ae4c73a5aee9cce65621245b47ae`  
		Last Modified: Fri, 06 May 2022 00:41:35 GMT  
		Size: 6.6 MB (6616060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3820c41861a9c3a37250697cb7e7fdf4e4cc80f0bd9c178d745f027a8a0d131d`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2535fcfc181880522bf4850c1225697df6558a460f38463f088d913c7e12a`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955231fc6b6d87f1db4f6969d0124c7c4128ae1b6eb86f1a6ccacf5d45ecaa3`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcef5c1f0ef015bb15178968436edb351493c6dfbc2cc991519fb9ffa677a2a`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 1.2 MB (1177962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4176a0bf28450b44c81df0cb8037d4f8243db5e12bf75e94d615fee11feb1c3`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e056e9920334b032414178275b4b31b88819db068254942117848ddcb4de7c`  
		Last Modified: Fri, 06 May 2022 00:41:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef81f82cb8cafcd766fb32f092fb9ae8490cdac5e0d8fdcfd1bd136735f7c6f`  
		Last Modified: Fri, 06 May 2022 00:42:00 GMT  
		Size: 21.2 MB (21178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd6a71a1f89738fb89ac09a875bd7c4c77ae3dbf7fef846b5cf734514c649d3`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:c90dd9e5207c28ebe553c5f3c22800f23b47fbf842764da58b43999f2819c99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:2a95fb5fb806607fa39f25d94a7de003aab8040f8623e03b4434c8a084a4aa14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668d0ecb09af29b085f8e3c1311c8f0ffa2262544158e522a0ebcc3a6756a5b`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:03:24 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ad07c68c8e389d0cd313e11a85df9558ac2048becd37904cf1917e1874ee33`  
		Last Modified: Tue, 05 Apr 2022 11:05:05 GMT  
		Size: 6.8 MB (6824112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d8935f9ab7676111d34aba704bf2993f1ca3bc71966e293eb7b1e7117fc6bff4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71566353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e01a98e8766126249fb7c3fdbd5bdecb77b0ebf999d9bf77fbf81097a614a2`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:40:24 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ca48e10901a8c88c7e63d41bb9939f8b45b851cb33a71ee5d4759e99ea418`  
		Last Modified: Fri, 06 May 2022 00:42:21 GMT  
		Size: 6.9 MB (6935709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:d258e77276a1a04a9625710d3a4260d832d7a1160ba2b3925d2b5d056df2bb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `docker:20-windowsservercore` - windows version 10.0.20348.643; amd64

```console
$ docker pull docker@sha256:fff694b8e04634839d70b3dfe7df104ad5534468ca98045d5a8afac643a2a6db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2281425027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a5211ccf13b003be0b83bdcc11c10e78c678f99b447d4b31a9b8ee3f354978`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:53:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:53:41 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:53:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:54:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214a200bfffc3a07addfc26100cb111b878672dab66c4783d9130c9c1368804`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 627.9 KB (627901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30b4c4063682b1a627c15d4272a77431260ca06226d48bcb01ecec36fddc82a`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc258b4f0c17f5025bc4293e83eda411702017e5eff5de41fd744d24427867d`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2a3d2481445420779bbb18707a79b51f161df7672019ac72ce1cbda63500b7`  
		Last Modified: Wed, 13 Apr 2022 18:58:38 GMT  
		Size: 53.8 MB (53838047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull docker@sha256:f3714b84a387d3897f180235aadce776774798d4f394f44a405f17d8c1929db3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769895637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c67d6ad6f01b9e1397beb07301451929fd69133247b0909b8fcc8206740280e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:55:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:55:58 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:55:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:57:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181d542854f38ea0a4a21bbed1dc9ed1475a2e4e4ce2bca7f65258aae0e626d`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 364.3 KB (364252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bb615d8550327c53488febde5e688f6089af17c006de3f81239daac1db82a`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7a7fd5c743b0106388ee4cc511d22e686f07c88bc1c78315c3f86566626abe`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a708ff879c76b4a6402649789b43994b88a410f169331e300c80ccb3375cb8`  
		Last Modified: Wed, 13 Apr 2022 18:59:06 GMT  
		Size: 53.6 MB (53606816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:1d46aa0a32d316d4f40e4cf5aee286878a6f0c527b24d9934b6035e24864621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull docker@sha256:f3714b84a387d3897f180235aadce776774798d4f394f44a405f17d8c1929db3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769895637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c67d6ad6f01b9e1397beb07301451929fd69133247b0909b8fcc8206740280e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:55:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:55:58 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:55:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:57:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181d542854f38ea0a4a21bbed1dc9ed1475a2e4e4ce2bca7f65258aae0e626d`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 364.3 KB (364252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bb615d8550327c53488febde5e688f6089af17c006de3f81239daac1db82a`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7a7fd5c743b0106388ee4cc511d22e686f07c88bc1c78315c3f86566626abe`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a708ff879c76b4a6402649789b43994b88a410f169331e300c80ccb3375cb8`  
		Last Modified: Wed, 13 Apr 2022 18:59:06 GMT  
		Size: 53.6 MB (53606816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ed4f3e2f83acb261c846cb191bee30f0a103c011ad5900fa0b8c29493bbefb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `docker:20-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull docker@sha256:fff694b8e04634839d70b3dfe7df104ad5534468ca98045d5a8afac643a2a6db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2281425027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a5211ccf13b003be0b83bdcc11c10e78c678f99b447d4b31a9b8ee3f354978`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:53:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:53:41 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:53:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:54:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214a200bfffc3a07addfc26100cb111b878672dab66c4783d9130c9c1368804`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 627.9 KB (627901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30b4c4063682b1a627c15d4272a77431260ca06226d48bcb01ecec36fddc82a`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc258b4f0c17f5025bc4293e83eda411702017e5eff5de41fd744d24427867d`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2a3d2481445420779bbb18707a79b51f161df7672019ac72ce1cbda63500b7`  
		Last Modified: Wed, 13 Apr 2022 18:58:38 GMT  
		Size: 53.8 MB (53838047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:ae371e93d152b87afd483252230fe4d9a4fb860d22fbfd952cec9d9890024b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:01b5f40cce1c35af66084493234610a03024efa5ed68376738d28348363a4692
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69397588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7417809fdb730b60c1b903077030aacc708677cdf02f2416ce413f38e81ec7e0`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7896b5013b29f7939347c46f6f4167286179e35d39defa227bde90ede9b8fb14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64630644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4276b804610ccca519b2419f29c4d8b08a9fe66221dfccb94342683a2f8a8407`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:56f24b157d2335f82fb3b2b22a0bacfe8c4bf3aacc273c806e4d53bbb1255a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:dd3584c00ebb822729dd5d2902e3a579ca87b9590637b5175035c1b05ea2fec0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76137359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a072474332af3e4cf06e349685c4cea8f9e631f0c5cab5b582f3a3ab4cff9b6a`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:02:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Apr 2022 11:02:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:02:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Apr 2022 11:02:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Apr 2022 11:02:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:57 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Apr 2022 11:02:57 GMT
EXPOSE 2375 2376
# Tue, 05 Apr 2022 11:02:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:57 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0af8a24b3d99f5d1b97b69005e6e5e973fd76878eb63382937c166cdf5441e`  
		Last Modified: Tue, 05 Apr 2022 11:04:16 GMT  
		Size: 6.7 MB (6734743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c69def9f2284d6ca51f913d19f45240f7051c275501a791efcbf2390a18704`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2998284497aa95875ef53929de1b46642eec185be6f5dd1a1e772dbce1761102`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67900e1c727f6291a49060673983d9297ce9a47b8e599f10fb276e8ff7973f4f`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 2.7 KB (2748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:333ea2510abe899d7c9f57fbd47d94b4300e46ea1b9972beb14aa0c5867bba13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62dcf8507f3db88fb2e57abaac240a09ea1c7157da93e46836b1d297b7f47a0`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 06 May 2022 00:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 06 May 2022 00:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 06 May 2022 00:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:57 GMT
VOLUME [/var/lib/docker]
# Fri, 06 May 2022 00:39:58 GMT
EXPOSE 2375 2376
# Fri, 06 May 2022 00:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 06 May 2022 00:40:00 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc82fabc8945c86cefb751ae77c8dd196e1ae4c73a5aee9cce65621245b47ae`  
		Last Modified: Fri, 06 May 2022 00:41:35 GMT  
		Size: 6.6 MB (6616060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3820c41861a9c3a37250697cb7e7fdf4e4cc80f0bd9c178d745f027a8a0d131d`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2535fcfc181880522bf4850c1225697df6558a460f38463f088d913c7e12a`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955231fc6b6d87f1db4f6969d0124c7c4128ae1b6eb86f1a6ccacf5d45ecaa3`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:d8fb0f5505924b4e7c520e9e1115d58be5fd6e752d1ae1e0f22dd76c758b2a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d1a3e15aeecebf41c8d9b00747ed033cd946c48645af94d9ee4e1c80ade2bb6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96432886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deda3d6ded5613af44013e788c53e5a0d7e86079e756c6b9014b1b4e7f8a73a9`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:02:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Apr 2022 11:02:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:02:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Apr 2022 11:02:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Apr 2022 11:02:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:57 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Apr 2022 11:02:57 GMT
EXPOSE 2375 2376
# Tue, 05 Apr 2022 11:02:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:57 GMT
CMD []
# Tue, 05 Apr 2022 11:03:01 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Apr 2022 11:03:02 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Apr 2022 11:03:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:03:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Apr 2022 11:03:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Apr 2022 11:03:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Apr 2022 11:03:19 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0af8a24b3d99f5d1b97b69005e6e5e973fd76878eb63382937c166cdf5441e`  
		Last Modified: Tue, 05 Apr 2022 11:04:16 GMT  
		Size: 6.7 MB (6734743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c69def9f2284d6ca51f913d19f45240f7051c275501a791efcbf2390a18704`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2998284497aa95875ef53929de1b46642eec185be6f5dd1a1e772dbce1761102`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67900e1c727f6291a49060673983d9297ce9a47b8e599f10fb276e8ff7973f4f`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 2.7 KB (2748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b588ce9e8fbc77fa67055ed6052e4298508b1fb1b243a0c235fe33418ebaf1c5`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 1.2 MB (1161981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1b74acd02dbc4e96821b38c1e1c58a37727ed03f82437cab1656c15e1d5b16`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b219f357717a1ca5ecae5a8f6141cb714f5782dc31f2ceaa63c7da45c89a42`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e307cac3961eec1242ccb911c3fb275f1287855f424c45c1d79e7edb756a4b89`  
		Last Modified: Tue, 05 Apr 2022 11:04:46 GMT  
		Size: 19.1 MB (19131830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11dca8585ce11aea5a2421a5b4d5d811c7ac4669e739d034620f7f2a7ef23c3`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f87b7f70c9a48c367e5927e328e1b315ec801cc2bde914c380eb220e697eea8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93609717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36974783d1fa9b40e54da0c7835c50e25ec6ba9dd36ece5f4676eaed997cf099`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 06 May 2022 00:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 06 May 2022 00:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 06 May 2022 00:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:57 GMT
VOLUME [/var/lib/docker]
# Fri, 06 May 2022 00:39:58 GMT
EXPOSE 2375 2376
# Fri, 06 May 2022 00:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 06 May 2022 00:40:00 GMT
CMD []
# Fri, 06 May 2022 00:40:08 GMT
RUN apk add --no-cache iproute2
# Fri, 06 May 2022 00:40:09 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 06 May 2022 00:40:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 06 May 2022 00:40:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 06 May 2022 00:40:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 06 May 2022 00:40:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 06 May 2022 00:40:16 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc82fabc8945c86cefb751ae77c8dd196e1ae4c73a5aee9cce65621245b47ae`  
		Last Modified: Fri, 06 May 2022 00:41:35 GMT  
		Size: 6.6 MB (6616060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3820c41861a9c3a37250697cb7e7fdf4e4cc80f0bd9c178d745f027a8a0d131d`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2535fcfc181880522bf4850c1225697df6558a460f38463f088d913c7e12a`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955231fc6b6d87f1db4f6969d0124c7c4128ae1b6eb86f1a6ccacf5d45ecaa3`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcef5c1f0ef015bb15178968436edb351493c6dfbc2cc991519fb9ffa677a2a`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 1.2 MB (1177962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4176a0bf28450b44c81df0cb8037d4f8243db5e12bf75e94d615fee11feb1c3`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e056e9920334b032414178275b4b31b88819db068254942117848ddcb4de7c`  
		Last Modified: Fri, 06 May 2022 00:41:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef81f82cb8cafcd766fb32f092fb9ae8490cdac5e0d8fdcfd1bd136735f7c6f`  
		Last Modified: Fri, 06 May 2022 00:42:00 GMT  
		Size: 21.2 MB (21178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd6a71a1f89738fb89ac09a875bd7c4c77ae3dbf7fef846b5cf734514c649d3`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:c90dd9e5207c28ebe553c5f3c22800f23b47fbf842764da58b43999f2819c99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:2a95fb5fb806607fa39f25d94a7de003aab8040f8623e03b4434c8a084a4aa14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668d0ecb09af29b085f8e3c1311c8f0ffa2262544158e522a0ebcc3a6756a5b`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:03:24 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ad07c68c8e389d0cd313e11a85df9558ac2048becd37904cf1917e1874ee33`  
		Last Modified: Tue, 05 Apr 2022 11:05:05 GMT  
		Size: 6.8 MB (6824112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d8935f9ab7676111d34aba704bf2993f1ca3bc71966e293eb7b1e7117fc6bff4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71566353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e01a98e8766126249fb7c3fdbd5bdecb77b0ebf999d9bf77fbf81097a614a2`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:40:24 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ca48e10901a8c88c7e63d41bb9939f8b45b851cb33a71ee5d4759e99ea418`  
		Last Modified: Fri, 06 May 2022 00:42:21 GMT  
		Size: 6.9 MB (6935709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:d258e77276a1a04a9625710d3a4260d832d7a1160ba2b3925d2b5d056df2bb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.20348.643; amd64

```console
$ docker pull docker@sha256:fff694b8e04634839d70b3dfe7df104ad5534468ca98045d5a8afac643a2a6db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2281425027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a5211ccf13b003be0b83bdcc11c10e78c678f99b447d4b31a9b8ee3f354978`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:53:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:53:41 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:53:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:54:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214a200bfffc3a07addfc26100cb111b878672dab66c4783d9130c9c1368804`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 627.9 KB (627901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30b4c4063682b1a627c15d4272a77431260ca06226d48bcb01ecec36fddc82a`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc258b4f0c17f5025bc4293e83eda411702017e5eff5de41fd744d24427867d`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2a3d2481445420779bbb18707a79b51f161df7672019ac72ce1cbda63500b7`  
		Last Modified: Wed, 13 Apr 2022 18:58:38 GMT  
		Size: 53.8 MB (53838047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull docker@sha256:f3714b84a387d3897f180235aadce776774798d4f394f44a405f17d8c1929db3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769895637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c67d6ad6f01b9e1397beb07301451929fd69133247b0909b8fcc8206740280e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:55:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:55:58 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:55:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:57:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181d542854f38ea0a4a21bbed1dc9ed1475a2e4e4ce2bca7f65258aae0e626d`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 364.3 KB (364252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bb615d8550327c53488febde5e688f6089af17c006de3f81239daac1db82a`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7a7fd5c743b0106388ee4cc511d22e686f07c88bc1c78315c3f86566626abe`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a708ff879c76b4a6402649789b43994b88a410f169331e300c80ccb3375cb8`  
		Last Modified: Wed, 13 Apr 2022 18:59:06 GMT  
		Size: 53.6 MB (53606816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:1d46aa0a32d316d4f40e4cf5aee286878a6f0c527b24d9934b6035e24864621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull docker@sha256:f3714b84a387d3897f180235aadce776774798d4f394f44a405f17d8c1929db3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769895637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c67d6ad6f01b9e1397beb07301451929fd69133247b0909b8fcc8206740280e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:55:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:55:58 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:55:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:57:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181d542854f38ea0a4a21bbed1dc9ed1475a2e4e4ce2bca7f65258aae0e626d`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 364.3 KB (364252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bb615d8550327c53488febde5e688f6089af17c006de3f81239daac1db82a`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7a7fd5c743b0106388ee4cc511d22e686f07c88bc1c78315c3f86566626abe`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a708ff879c76b4a6402649789b43994b88a410f169331e300c80ccb3375cb8`  
		Last Modified: Wed, 13 Apr 2022 18:59:06 GMT  
		Size: 53.6 MB (53606816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ed4f3e2f83acb261c846cb191bee30f0a103c011ad5900fa0b8c29493bbefb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `docker:20.10-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull docker@sha256:fff694b8e04634839d70b3dfe7df104ad5534468ca98045d5a8afac643a2a6db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2281425027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a5211ccf13b003be0b83bdcc11c10e78c678f99b447d4b31a9b8ee3f354978`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:53:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:53:41 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:53:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:54:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214a200bfffc3a07addfc26100cb111b878672dab66c4783d9130c9c1368804`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 627.9 KB (627901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30b4c4063682b1a627c15d4272a77431260ca06226d48bcb01ecec36fddc82a`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc258b4f0c17f5025bc4293e83eda411702017e5eff5de41fd744d24427867d`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2a3d2481445420779bbb18707a79b51f161df7672019ac72ce1cbda63500b7`  
		Last Modified: Wed, 13 Apr 2022 18:58:38 GMT  
		Size: 53.8 MB (53838047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.15`

```console
$ docker pull docker@sha256:27ec56bb23814ef0834861eb8f48a4077ab32b3d9d701a47ca2a6f79f160287a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:20.10.15` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7896b5013b29f7939347c46f6f4167286179e35d39defa227bde90ede9b8fb14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64630644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4276b804610ccca519b2419f29c4d8b08a9fe66221dfccb94342683a2f8a8407`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.15-alpine3.15`

```console
$ docker pull docker@sha256:27ec56bb23814ef0834861eb8f48a4077ab32b3d9d701a47ca2a6f79f160287a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:20.10.15-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7896b5013b29f7939347c46f6f4167286179e35d39defa227bde90ede9b8fb14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64630644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4276b804610ccca519b2419f29c4d8b08a9fe66221dfccb94342683a2f8a8407`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.15-dind`

```console
$ docker pull docker@sha256:c67c91390b1260706cf61fe429e0047ddfde34bb6cc9cd27bfc6d0e164620abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:20.10.15-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:333ea2510abe899d7c9f57fbd47d94b4300e46ea1b9972beb14aa0c5867bba13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62dcf8507f3db88fb2e57abaac240a09ea1c7157da93e46836b1d297b7f47a0`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 06 May 2022 00:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 06 May 2022 00:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 06 May 2022 00:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:57 GMT
VOLUME [/var/lib/docker]
# Fri, 06 May 2022 00:39:58 GMT
EXPOSE 2375 2376
# Fri, 06 May 2022 00:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 06 May 2022 00:40:00 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc82fabc8945c86cefb751ae77c8dd196e1ae4c73a5aee9cce65621245b47ae`  
		Last Modified: Fri, 06 May 2022 00:41:35 GMT  
		Size: 6.6 MB (6616060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3820c41861a9c3a37250697cb7e7fdf4e4cc80f0bd9c178d745f027a8a0d131d`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2535fcfc181880522bf4850c1225697df6558a460f38463f088d913c7e12a`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955231fc6b6d87f1db4f6969d0124c7c4128ae1b6eb86f1a6ccacf5d45ecaa3`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.15-dind-alpine3.15`

```console
$ docker pull docker@sha256:c67c91390b1260706cf61fe429e0047ddfde34bb6cc9cd27bfc6d0e164620abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:20.10.15-dind-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:333ea2510abe899d7c9f57fbd47d94b4300e46ea1b9972beb14aa0c5867bba13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62dcf8507f3db88fb2e57abaac240a09ea1c7157da93e46836b1d297b7f47a0`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 06 May 2022 00:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 06 May 2022 00:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 06 May 2022 00:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:57 GMT
VOLUME [/var/lib/docker]
# Fri, 06 May 2022 00:39:58 GMT
EXPOSE 2375 2376
# Fri, 06 May 2022 00:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 06 May 2022 00:40:00 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc82fabc8945c86cefb751ae77c8dd196e1ae4c73a5aee9cce65621245b47ae`  
		Last Modified: Fri, 06 May 2022 00:41:35 GMT  
		Size: 6.6 MB (6616060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3820c41861a9c3a37250697cb7e7fdf4e4cc80f0bd9c178d745f027a8a0d131d`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2535fcfc181880522bf4850c1225697df6558a460f38463f088d913c7e12a`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955231fc6b6d87f1db4f6969d0124c7c4128ae1b6eb86f1a6ccacf5d45ecaa3`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.15-dind-rootless`

```console
$ docker pull docker@sha256:7a2e428c5b06bb95e21204f46cb327c05cffc5c6e621331a2b4cc23c1a2d76c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:20.10.15-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f87b7f70c9a48c367e5927e328e1b315ec801cc2bde914c380eb220e697eea8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93609717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36974783d1fa9b40e54da0c7835c50e25ec6ba9dd36ece5f4676eaed997cf099`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 06 May 2022 00:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 06 May 2022 00:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 06 May 2022 00:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:57 GMT
VOLUME [/var/lib/docker]
# Fri, 06 May 2022 00:39:58 GMT
EXPOSE 2375 2376
# Fri, 06 May 2022 00:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 06 May 2022 00:40:00 GMT
CMD []
# Fri, 06 May 2022 00:40:08 GMT
RUN apk add --no-cache iproute2
# Fri, 06 May 2022 00:40:09 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 06 May 2022 00:40:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 06 May 2022 00:40:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 06 May 2022 00:40:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 06 May 2022 00:40:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 06 May 2022 00:40:16 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc82fabc8945c86cefb751ae77c8dd196e1ae4c73a5aee9cce65621245b47ae`  
		Last Modified: Fri, 06 May 2022 00:41:35 GMT  
		Size: 6.6 MB (6616060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3820c41861a9c3a37250697cb7e7fdf4e4cc80f0bd9c178d745f027a8a0d131d`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2535fcfc181880522bf4850c1225697df6558a460f38463f088d913c7e12a`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955231fc6b6d87f1db4f6969d0124c7c4128ae1b6eb86f1a6ccacf5d45ecaa3`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcef5c1f0ef015bb15178968436edb351493c6dfbc2cc991519fb9ffa677a2a`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 1.2 MB (1177962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4176a0bf28450b44c81df0cb8037d4f8243db5e12bf75e94d615fee11feb1c3`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e056e9920334b032414178275b4b31b88819db068254942117848ddcb4de7c`  
		Last Modified: Fri, 06 May 2022 00:41:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef81f82cb8cafcd766fb32f092fb9ae8490cdac5e0d8fdcfd1bd136735f7c6f`  
		Last Modified: Fri, 06 May 2022 00:42:00 GMT  
		Size: 21.2 MB (21178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd6a71a1f89738fb89ac09a875bd7c4c77ae3dbf7fef846b5cf734514c649d3`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.15-git`

```console
$ docker pull docker@sha256:f7b8ffd9fed551ba7bc08abe25b51e9582386ed145c4d224e4dbed49bf9a0288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:20.10.15-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d8935f9ab7676111d34aba704bf2993f1ca3bc71966e293eb7b1e7117fc6bff4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71566353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e01a98e8766126249fb7c3fdbd5bdecb77b0ebf999d9bf77fbf81097a614a2`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:40:24 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ca48e10901a8c88c7e63d41bb9939f8b45b851cb33a71ee5d4759e99ea418`  
		Last Modified: Fri, 06 May 2022 00:42:21 GMT  
		Size: 6.9 MB (6935709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.15-windowsservercore`

```console
$ docker pull docker@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `docker:20.10.15-windowsservercore-1809`

```console
$ docker pull docker@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `docker:20.10.15-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `docker:dind`

```console
$ docker pull docker@sha256:56f24b157d2335f82fb3b2b22a0bacfe8c4bf3aacc273c806e4d53bbb1255a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:dd3584c00ebb822729dd5d2902e3a579ca87b9590637b5175035c1b05ea2fec0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76137359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a072474332af3e4cf06e349685c4cea8f9e631f0c5cab5b582f3a3ab4cff9b6a`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:02:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Apr 2022 11:02:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:02:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Apr 2022 11:02:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Apr 2022 11:02:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:57 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Apr 2022 11:02:57 GMT
EXPOSE 2375 2376
# Tue, 05 Apr 2022 11:02:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:57 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0af8a24b3d99f5d1b97b69005e6e5e973fd76878eb63382937c166cdf5441e`  
		Last Modified: Tue, 05 Apr 2022 11:04:16 GMT  
		Size: 6.7 MB (6734743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c69def9f2284d6ca51f913d19f45240f7051c275501a791efcbf2390a18704`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2998284497aa95875ef53929de1b46642eec185be6f5dd1a1e772dbce1761102`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67900e1c727f6291a49060673983d9297ce9a47b8e599f10fb276e8ff7973f4f`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 2.7 KB (2748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:333ea2510abe899d7c9f57fbd47d94b4300e46ea1b9972beb14aa0c5867bba13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62dcf8507f3db88fb2e57abaac240a09ea1c7157da93e46836b1d297b7f47a0`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 06 May 2022 00:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 06 May 2022 00:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 06 May 2022 00:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:57 GMT
VOLUME [/var/lib/docker]
# Fri, 06 May 2022 00:39:58 GMT
EXPOSE 2375 2376
# Fri, 06 May 2022 00:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 06 May 2022 00:40:00 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc82fabc8945c86cefb751ae77c8dd196e1ae4c73a5aee9cce65621245b47ae`  
		Last Modified: Fri, 06 May 2022 00:41:35 GMT  
		Size: 6.6 MB (6616060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3820c41861a9c3a37250697cb7e7fdf4e4cc80f0bd9c178d745f027a8a0d131d`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2535fcfc181880522bf4850c1225697df6558a460f38463f088d913c7e12a`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955231fc6b6d87f1db4f6969d0124c7c4128ae1b6eb86f1a6ccacf5d45ecaa3`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:d8fb0f5505924b4e7c520e9e1115d58be5fd6e752d1ae1e0f22dd76c758b2a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d1a3e15aeecebf41c8d9b00747ed033cd946c48645af94d9ee4e1c80ade2bb6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96432886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deda3d6ded5613af44013e788c53e5a0d7e86079e756c6b9014b1b4e7f8a73a9`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:02:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Apr 2022 11:02:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:02:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Apr 2022 11:02:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Apr 2022 11:02:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:57 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Apr 2022 11:02:57 GMT
EXPOSE 2375 2376
# Tue, 05 Apr 2022 11:02:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:57 GMT
CMD []
# Tue, 05 Apr 2022 11:03:01 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Apr 2022 11:03:02 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Apr 2022 11:03:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:03:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Apr 2022 11:03:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Apr 2022 11:03:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Apr 2022 11:03:19 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0af8a24b3d99f5d1b97b69005e6e5e973fd76878eb63382937c166cdf5441e`  
		Last Modified: Tue, 05 Apr 2022 11:04:16 GMT  
		Size: 6.7 MB (6734743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c69def9f2284d6ca51f913d19f45240f7051c275501a791efcbf2390a18704`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2998284497aa95875ef53929de1b46642eec185be6f5dd1a1e772dbce1761102`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67900e1c727f6291a49060673983d9297ce9a47b8e599f10fb276e8ff7973f4f`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 2.7 KB (2748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b588ce9e8fbc77fa67055ed6052e4298508b1fb1b243a0c235fe33418ebaf1c5`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 1.2 MB (1161981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1b74acd02dbc4e96821b38c1e1c58a37727ed03f82437cab1656c15e1d5b16`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b219f357717a1ca5ecae5a8f6141cb714f5782dc31f2ceaa63c7da45c89a42`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e307cac3961eec1242ccb911c3fb275f1287855f424c45c1d79e7edb756a4b89`  
		Last Modified: Tue, 05 Apr 2022 11:04:46 GMT  
		Size: 19.1 MB (19131830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11dca8585ce11aea5a2421a5b4d5d811c7ac4669e739d034620f7f2a7ef23c3`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f87b7f70c9a48c367e5927e328e1b315ec801cc2bde914c380eb220e697eea8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93609717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36974783d1fa9b40e54da0c7835c50e25ec6ba9dd36ece5f4676eaed997cf099`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 06 May 2022 00:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 06 May 2022 00:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 06 May 2022 00:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 06 May 2022 00:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:57 GMT
VOLUME [/var/lib/docker]
# Fri, 06 May 2022 00:39:58 GMT
EXPOSE 2375 2376
# Fri, 06 May 2022 00:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 06 May 2022 00:40:00 GMT
CMD []
# Fri, 06 May 2022 00:40:08 GMT
RUN apk add --no-cache iproute2
# Fri, 06 May 2022 00:40:09 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 06 May 2022 00:40:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 06 May 2022 00:40:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 06 May 2022 00:40:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 06 May 2022 00:40:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 06 May 2022 00:40:16 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc82fabc8945c86cefb751ae77c8dd196e1ae4c73a5aee9cce65621245b47ae`  
		Last Modified: Fri, 06 May 2022 00:41:35 GMT  
		Size: 6.6 MB (6616060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3820c41861a9c3a37250697cb7e7fdf4e4cc80f0bd9c178d745f027a8a0d131d`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f2535fcfc181880522bf4850c1225697df6558a460f38463f088d913c7e12a`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955231fc6b6d87f1db4f6969d0124c7c4128ae1b6eb86f1a6ccacf5d45ecaa3`  
		Last Modified: Fri, 06 May 2022 00:41:34 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcef5c1f0ef015bb15178968436edb351493c6dfbc2cc991519fb9ffa677a2a`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 1.2 MB (1177962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4176a0bf28450b44c81df0cb8037d4f8243db5e12bf75e94d615fee11feb1c3`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e056e9920334b032414178275b4b31b88819db068254942117848ddcb4de7c`  
		Last Modified: Fri, 06 May 2022 00:41:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef81f82cb8cafcd766fb32f092fb9ae8490cdac5e0d8fdcfd1bd136735f7c6f`  
		Last Modified: Fri, 06 May 2022 00:42:00 GMT  
		Size: 21.2 MB (21178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd6a71a1f89738fb89ac09a875bd7c4c77ae3dbf7fef846b5cf734514c649d3`  
		Last Modified: Fri, 06 May 2022 00:41:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:c90dd9e5207c28ebe553c5f3c22800f23b47fbf842764da58b43999f2819c99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:2a95fb5fb806607fa39f25d94a7de003aab8040f8623e03b4434c8a084a4aa14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668d0ecb09af29b085f8e3c1311c8f0ffa2262544158e522a0ebcc3a6756a5b`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:03:24 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ad07c68c8e389d0cd313e11a85df9558ac2048becd37904cf1917e1874ee33`  
		Last Modified: Tue, 05 Apr 2022 11:05:05 GMT  
		Size: 6.8 MB (6824112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d8935f9ab7676111d34aba704bf2993f1ca3bc71966e293eb7b1e7117fc6bff4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71566353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e01a98e8766126249fb7c3fdbd5bdecb77b0ebf999d9bf77fbf81097a614a2`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
CMD ["sh"]
# Fri, 06 May 2022 00:40:24 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ca48e10901a8c88c7e63d41bb9939f8b45b851cb33a71ee5d4759e99ea418`  
		Last Modified: Fri, 06 May 2022 00:42:21 GMT  
		Size: 6.9 MB (6935709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:ae371e93d152b87afd483252230fe4d9a4fb860d22fbfd952cec9d9890024b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:01b5f40cce1c35af66084493234610a03024efa5ed68376738d28348363a4692
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69397588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7417809fdb730b60c1b903077030aacc708677cdf02f2416ce413f38e81ec7e0`
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
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
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
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7896b5013b29f7939347c46f6f4167286179e35d39defa227bde90ede9b8fb14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64630644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4276b804610ccca519b2419f29c4d8b08a9fe66221dfccb94342683a2f8a8407`
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
# Fri, 06 May 2022 00:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 06 May 2022 00:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 06 May 2022 00:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 06 May 2022 00:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 06 May 2022 00:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 May 2022 00:39:43 GMT
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
	-	`sha256:5c620ef89e70dfd8ee45478c40df37fa3978a3834d62e9caaf6ea8784f194223`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932fe59f5c2c048a3fe96c5a302bbec8674ad62617d71cda26f29fb956b3df14`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e4e555ced57a6c5995c7c6c1e13e86a169af3622bf5a764d4eee0bdd94d30b`  
		Last Modified: Fri, 06 May 2022 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:d258e77276a1a04a9625710d3a4260d832d7a1160ba2b3925d2b5d056df2bb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `docker:windowsservercore` - windows version 10.0.20348.643; amd64

```console
$ docker pull docker@sha256:fff694b8e04634839d70b3dfe7df104ad5534468ca98045d5a8afac643a2a6db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2281425027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a5211ccf13b003be0b83bdcc11c10e78c678f99b447d4b31a9b8ee3f354978`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:53:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:53:41 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:53:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:54:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214a200bfffc3a07addfc26100cb111b878672dab66c4783d9130c9c1368804`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 627.9 KB (627901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30b4c4063682b1a627c15d4272a77431260ca06226d48bcb01ecec36fddc82a`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc258b4f0c17f5025bc4293e83eda411702017e5eff5de41fd744d24427867d`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2a3d2481445420779bbb18707a79b51f161df7672019ac72ce1cbda63500b7`  
		Last Modified: Wed, 13 Apr 2022 18:58:38 GMT  
		Size: 53.8 MB (53838047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull docker@sha256:f3714b84a387d3897f180235aadce776774798d4f394f44a405f17d8c1929db3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769895637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c67d6ad6f01b9e1397beb07301451929fd69133247b0909b8fcc8206740280e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:55:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:55:58 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:55:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:57:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181d542854f38ea0a4a21bbed1dc9ed1475a2e4e4ce2bca7f65258aae0e626d`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 364.3 KB (364252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bb615d8550327c53488febde5e688f6089af17c006de3f81239daac1db82a`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7a7fd5c743b0106388ee4cc511d22e686f07c88bc1c78315c3f86566626abe`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a708ff879c76b4a6402649789b43994b88a410f169331e300c80ccb3375cb8`  
		Last Modified: Wed, 13 Apr 2022 18:59:06 GMT  
		Size: 53.6 MB (53606816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:1d46aa0a32d316d4f40e4cf5aee286878a6f0c527b24d9934b6035e24864621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull docker@sha256:f3714b84a387d3897f180235aadce776774798d4f394f44a405f17d8c1929db3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769895637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c67d6ad6f01b9e1397beb07301451929fd69133247b0909b8fcc8206740280e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:55:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:55:58 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:55:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:57:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181d542854f38ea0a4a21bbed1dc9ed1475a2e4e4ce2bca7f65258aae0e626d`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 364.3 KB (364252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bb615d8550327c53488febde5e688f6089af17c006de3f81239daac1db82a`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7a7fd5c743b0106388ee4cc511d22e686f07c88bc1c78315c3f86566626abe`  
		Last Modified: Wed, 13 Apr 2022 18:58:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a708ff879c76b4a6402649789b43994b88a410f169331e300c80ccb3375cb8`  
		Last Modified: Wed, 13 Apr 2022 18:59:06 GMT  
		Size: 53.6 MB (53606816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ed4f3e2f83acb261c846cb191bee30f0a103c011ad5900fa0b8c29493bbefb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull docker@sha256:fff694b8e04634839d70b3dfe7df104ad5534468ca98045d5a8afac643a2a6db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2281425027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a5211ccf13b003be0b83bdcc11c10e78c678f99b447d4b31a9b8ee3f354978`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:53:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:53:41 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:53:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:54:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214a200bfffc3a07addfc26100cb111b878672dab66c4783d9130c9c1368804`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 627.9 KB (627901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30b4c4063682b1a627c15d4272a77431260ca06226d48bcb01ecec36fddc82a`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc258b4f0c17f5025bc4293e83eda411702017e5eff5de41fd744d24427867d`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2a3d2481445420779bbb18707a79b51f161df7672019ac72ce1cbda63500b7`  
		Last Modified: Wed, 13 Apr 2022 18:58:38 GMT  
		Size: 53.8 MB (53838047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
