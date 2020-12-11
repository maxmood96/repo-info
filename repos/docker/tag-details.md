<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:19`](#docker19)
-	[`docker:19.03`](#docker1903)
-	[`docker:19.03.14`](#docker190314)
-	[`docker:19.03.14-dind`](#docker190314-dind)
-	[`docker:19.03.14-dind-rootless`](#docker190314-dind-rootless)
-	[`docker:19.03.14-git`](#docker190314-git)
-	[`docker:19.03-dind`](#docker1903-dind)
-	[`docker:19.03-dind-rootless`](#docker1903-dind-rootless)
-	[`docker:19.03-git`](#docker1903-git)
-	[`docker:19-dind`](#docker19-dind)
-	[`docker:19-dind-rootless`](#docker19-dind-rootless)
-	[`docker:19-git`](#docker19-git)
-	[`docker:20`](#docker20)
-	[`docker:20.10`](#docker2010)
-	[`docker:20.10.0`](#docker20100)
-	[`docker:20.10.0-dind`](#docker20100-dind)
-	[`docker:20.10.0-dind-rootless`](#docker20100-dind-rootless)
-	[`docker:20.10.0-git`](#docker20100-git)
-	[`docker:20.10-dind`](#docker2010-dind)
-	[`docker:20.10-dind-rootless`](#docker2010-dind-rootless)
-	[`docker:20.10-git`](#docker2010-git)
-	[`docker:20-dind`](#docker20-dind)
-	[`docker:20-dind-rootless`](#docker20-dind-rootless)
-	[`docker:20-git`](#docker20-git)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)

## `docker:19`

```console
$ docker pull docker@sha256:37d06c0dab789da956d3e922cf8e0bbcaf836d78179f11bce7db287c60b0fd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19` - linux; amd64

```console
$ docker pull docker@sha256:8f71deccd0856d8a36db659a8c82894be97546b47c1817de27d5ee7eea860162
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67728502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0757c55a1fdbb59c378fd34dde3e12bd25f68094dd69546cf5ca00ddbaa7a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v6

```console
$ docker pull docker@sha256:18d39b6848cecae067cc0d94c554029bfc88d3069c80bb5049d54da659249b94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3106fcafb44a465ee4e0efadc103e5018d57587bd5d5ba6f465846bf7c3844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce46ea18798c578f8923e0ced4c9996c30363fc35edd1b1c40e5e542407818ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a685736103d7a1e988f52fb20b130a353e545dff4ccd52c9b075d5ead6f11d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8eb49538a5ae25e1dcee16953ef182cf19d8c9d117300173ede2b7d88f173bbb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354327cb1b46abd394f47d0bd564e5018f821a33e8edfadce8114b879d30f9f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:43:16 GMT
ENV DOCKER_VERSION=19.03.14
# Fri, 11 Dec 2020 03:43:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:43:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:43:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:43:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:43:33 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44406ea375713a15815e70d9f67caccd9d24e3edb888eb33765a7855947a57dd`  
		Last Modified: Fri, 11 Dec 2020 03:46:07 GMT  
		Size: 56.0 MB (55992945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9e082087083b4fa5ee2804222088c41668d42a3cda42a0358add93cfbfed2`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11a145516582d37d1ac882ec6ced4d65ad928b3f5923c73b16211995c42da6`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961068b01d86e33d4e09c9fa6829e3ff7bdb7d3b6a60449681cdf49519058265`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03`

```console
$ docker pull docker@sha256:37d06c0dab789da956d3e922cf8e0bbcaf836d78179f11bce7db287c60b0fd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03` - linux; amd64

```console
$ docker pull docker@sha256:8f71deccd0856d8a36db659a8c82894be97546b47c1817de27d5ee7eea860162
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67728502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0757c55a1fdbb59c378fd34dde3e12bd25f68094dd69546cf5ca00ddbaa7a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v6

```console
$ docker pull docker@sha256:18d39b6848cecae067cc0d94c554029bfc88d3069c80bb5049d54da659249b94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3106fcafb44a465ee4e0efadc103e5018d57587bd5d5ba6f465846bf7c3844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce46ea18798c578f8923e0ced4c9996c30363fc35edd1b1c40e5e542407818ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a685736103d7a1e988f52fb20b130a353e545dff4ccd52c9b075d5ead6f11d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8eb49538a5ae25e1dcee16953ef182cf19d8c9d117300173ede2b7d88f173bbb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354327cb1b46abd394f47d0bd564e5018f821a33e8edfadce8114b879d30f9f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:43:16 GMT
ENV DOCKER_VERSION=19.03.14
# Fri, 11 Dec 2020 03:43:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:43:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:43:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:43:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:43:33 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44406ea375713a15815e70d9f67caccd9d24e3edb888eb33765a7855947a57dd`  
		Last Modified: Fri, 11 Dec 2020 03:46:07 GMT  
		Size: 56.0 MB (55992945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9e082087083b4fa5ee2804222088c41668d42a3cda42a0358add93cfbfed2`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11a145516582d37d1ac882ec6ced4d65ad928b3f5923c73b16211995c42da6`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961068b01d86e33d4e09c9fa6829e3ff7bdb7d3b6a60449681cdf49519058265`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.14`

```console
$ docker pull docker@sha256:8729a6b02ee78374c1de70f09fa21f004ba3dbe5bbd07407417c27eb25cc8b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:19.03.14` - linux; amd64

```console
$ docker pull docker@sha256:8f71deccd0856d8a36db659a8c82894be97546b47c1817de27d5ee7eea860162
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67728502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0757c55a1fdbb59c378fd34dde3e12bd25f68094dd69546cf5ca00ddbaa7a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8eb49538a5ae25e1dcee16953ef182cf19d8c9d117300173ede2b7d88f173bbb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354327cb1b46abd394f47d0bd564e5018f821a33e8edfadce8114b879d30f9f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:43:16 GMT
ENV DOCKER_VERSION=19.03.14
# Fri, 11 Dec 2020 03:43:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:43:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:43:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:43:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:43:33 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44406ea375713a15815e70d9f67caccd9d24e3edb888eb33765a7855947a57dd`  
		Last Modified: Fri, 11 Dec 2020 03:46:07 GMT  
		Size: 56.0 MB (55992945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9e082087083b4fa5ee2804222088c41668d42a3cda42a0358add93cfbfed2`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11a145516582d37d1ac882ec6ced4d65ad928b3f5923c73b16211995c42da6`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961068b01d86e33d4e09c9fa6829e3ff7bdb7d3b6a60449681cdf49519058265`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.14-dind`

```console
$ docker pull docker@sha256:a3760fe3543a2aa87da74fd9a2780497b6f95c1169ed6b09a505f2f76b27ce04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:19.03.14-dind` - linux; amd64

```console
$ docker pull docker@sha256:2a7e15ecad4d18a6bb71b1b828dc7bb1b1a6c890e7420a89726a0649e94e8fb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73691917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f19136cf89d49aee8fa560eaab20e034c6ee17bbce55a9d33e1fbe5baa35b03`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
# Wed, 02 Dec 2020 01:46:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 02 Dec 2020 01:46:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 02 Dec 2020 01:46:52 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Wed, 02 Dec 2020 01:46:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 02 Dec 2020 01:46:53 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:54 GMT
VOLUME [/var/lib/docker]
# Wed, 02 Dec 2020 01:46:54 GMT
EXPOSE 2375 2376
# Wed, 02 Dec 2020 01:46:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:54 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec33e9a5dc986ed79c57562e16a160920e60a9045ad42b230c8b3c3c2500937`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 6.0 MB (5958689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f95e189f660a26dc7fef2e6cb0cb97e5fd58a2cc3d94401ec05ec021b5d88ec`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48132e2f3ac7e59ba71722801162920cf61f245698f60bf839dc424199bbfceb`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b4df673d204888097abe33a208c939806155dbd1b8e08ea0f23b7dee721183`  
		Last Modified: Wed, 02 Dec 2020 01:47:58 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.14-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4f02c4ad7f9483dee2ebc9efe3c66633691504e4c3734fa38b657bb6beb22047
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66714139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c275ab420e15e0f0d3fe6e88b30424974332da758bf2804e204b73dc7a3ddb7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:43:16 GMT
ENV DOCKER_VERSION=19.03.14
# Fri, 11 Dec 2020 03:43:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:43:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:43:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:43:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:43:33 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:43:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 11 Dec 2020 03:43:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 11 Dec 2020 03:43:52 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Fri, 11 Dec 2020 03:43:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 11 Dec 2020 03:43:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:59 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Dec 2020 03:44:01 GMT
EXPOSE 2375 2376
# Fri, 11 Dec 2020 03:44:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Dec 2020 03:44:05 GMT
CMD []
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44406ea375713a15815e70d9f67caccd9d24e3edb888eb33765a7855947a57dd`  
		Last Modified: Fri, 11 Dec 2020 03:46:07 GMT  
		Size: 56.0 MB (55992945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9e082087083b4fa5ee2804222088c41668d42a3cda42a0358add93cfbfed2`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11a145516582d37d1ac882ec6ced4d65ad928b3f5923c73b16211995c42da6`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961068b01d86e33d4e09c9fa6829e3ff7bdb7d3b6a60449681cdf49519058265`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52bcec35351af8539981ca3f0097a0d3b02517a030e2fd5e2c52cd30c72ad66`  
		Last Modified: Fri, 11 Dec 2020 03:46:19 GMT  
		Size: 5.9 MB (5946714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba61fc8445e0471f06d03123c54a76ac7d5d292c0f9983e7021df62400b2d1`  
		Last Modified: Fri, 11 Dec 2020 03:46:19 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28426d0cbfd272b6cb9a64a8b6a1a41033edeae5823a4a809d71f5c1435d7a4`  
		Last Modified: Fri, 11 Dec 2020 03:46:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1827aa166b927762754e480784c7ca687bf2acf61142c2a4e9667cf203a63614`  
		Last Modified: Fri, 11 Dec 2020 03:46:18 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.14-dind-rootless`

```console
$ docker pull docker@sha256:4040c071ccf3194453d8a5a753138c9b0e630ec261eaa5824828003e543250a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03.14-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9ba6316c30560f8bfe973dce6f98709ab80a9333d4b20052950886de63cd673e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94208872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101be3479271665acafd3f369c3299037cadf6459f5d39f628893d2137351897`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
# Wed, 02 Dec 2020 01:46:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 02 Dec 2020 01:46:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 02 Dec 2020 01:46:52 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Wed, 02 Dec 2020 01:46:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 02 Dec 2020 01:46:53 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:54 GMT
VOLUME [/var/lib/docker]
# Wed, 02 Dec 2020 01:46:54 GMT
EXPOSE 2375 2376
# Wed, 02 Dec 2020 01:46:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:54 GMT
CMD []
# Wed, 02 Dec 2020 01:46:59 GMT
RUN apk add --no-cache iproute2
# Wed, 02 Dec 2020 01:47:00 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 02 Dec 2020 01:47:01 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 02 Dec 2020 01:47:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 02 Dec 2020 01:47:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 02 Dec 2020 01:47:05 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 02 Dec 2020 01:47:05 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec33e9a5dc986ed79c57562e16a160920e60a9045ad42b230c8b3c3c2500937`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 6.0 MB (5958689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f95e189f660a26dc7fef2e6cb0cb97e5fd58a2cc3d94401ec05ec021b5d88ec`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48132e2f3ac7e59ba71722801162920cf61f245698f60bf839dc424199bbfceb`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b4df673d204888097abe33a208c939806155dbd1b8e08ea0f23b7dee721183`  
		Last Modified: Wed, 02 Dec 2020 01:47:58 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b03ba64d7c79a3d1f862fe193765409f18ac16cc1b4d4574f25aa288a620296`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 1.1 MB (1092667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a006bc1e4e45e127971d77406f42aa0f538d329e88f95cfcff4b98abfdff2`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72211050ba3a0bd00e3a30db426b705249187eb5609f9f04b32789a2da46e5b`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a296f7783428cadcd8002da2013caaa0ca3ba2832c0b43f34977f2d654d6df6c`  
		Last Modified: Wed, 02 Dec 2020 01:48:11 GMT  
		Size: 19.4 MB (19422676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1110d8f13201e4039f28a0fbf83803b3c25b6fc2ee8fed96a15d2dc02f9b12ba`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.14-git`

```console
$ docker pull docker@sha256:da9d239eaaca225172eed7e85c585fbb2af70d94ac1902b1461e04b617eb0a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:19.03.14-git` - linux; amd64

```console
$ docker pull docker@sha256:3d7b7d06b06d4df7065f87a398737b006c55c1e789ea3fcbb1608f71f2f01e14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76040588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ed80ea9a6afb9549bdc68ddadd437dbd168ea952021a7a93e00f778f5dab00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
# Wed, 02 Dec 2020 01:47:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82826517bd937097d06a68b9e1bb91a60326d66a9e9071af3db93843edf4c0a2`  
		Last Modified: Wed, 02 Dec 2020 01:48:21 GMT  
		Size: 8.3 MB (8312086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.14-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31c852882a88e4c35ea2f1802f10d116fccbbe7101071d921c12e15beedd4cc4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69266142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae9478277bd44d0819627464380f1048579954877b0e7645ac34d954b63ab20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:43:16 GMT
ENV DOCKER_VERSION=19.03.14
# Fri, 11 Dec 2020 03:43:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:43:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:43:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:43:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:43:33 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:44:19 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44406ea375713a15815e70d9f67caccd9d24e3edb888eb33765a7855947a57dd`  
		Last Modified: Fri, 11 Dec 2020 03:46:07 GMT  
		Size: 56.0 MB (55992945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9e082087083b4fa5ee2804222088c41668d42a3cda42a0358add93cfbfed2`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11a145516582d37d1ac882ec6ced4d65ad928b3f5923c73b16211995c42da6`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961068b01d86e33d4e09c9fa6829e3ff7bdb7d3b6a60449681cdf49519058265`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72293c133127a3af2438e9fdec9f0453dd61056d294aec4c7c40b00a74c2e110`  
		Last Modified: Fri, 11 Dec 2020 03:46:31 GMT  
		Size: 8.5 MB (8503472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind`

```console
$ docker pull docker@sha256:8a1e6994b4b3f94056a49c85da69bf4480e27814a9c6121b196f9f0802b05ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-dind` - linux; amd64

```console
$ docker pull docker@sha256:2a7e15ecad4d18a6bb71b1b828dc7bb1b1a6c890e7420a89726a0649e94e8fb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73691917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f19136cf89d49aee8fa560eaab20e034c6ee17bbce55a9d33e1fbe5baa35b03`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
# Wed, 02 Dec 2020 01:46:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 02 Dec 2020 01:46:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 02 Dec 2020 01:46:52 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Wed, 02 Dec 2020 01:46:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 02 Dec 2020 01:46:53 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:54 GMT
VOLUME [/var/lib/docker]
# Wed, 02 Dec 2020 01:46:54 GMT
EXPOSE 2375 2376
# Wed, 02 Dec 2020 01:46:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:54 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec33e9a5dc986ed79c57562e16a160920e60a9045ad42b230c8b3c3c2500937`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 6.0 MB (5958689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f95e189f660a26dc7fef2e6cb0cb97e5fd58a2cc3d94401ec05ec021b5d88ec`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48132e2f3ac7e59ba71722801162920cf61f245698f60bf839dc424199bbfceb`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b4df673d204888097abe33a208c939806155dbd1b8e08ea0f23b7dee721183`  
		Last Modified: Wed, 02 Dec 2020 01:47:58 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6b0193cbf4d3c304f3bf6c6c253d88c25a22c6ffe6847fd57a6269e4324745f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a37c38067d51b4185a04675f81f45209b82449ce8bbbec68b31d639ba45cd5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 23 Apr 2020 17:13:24 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 23 Apr 2020 17:13:25 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 23 Apr 2020 17:13:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:49:37 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:49:38 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:49:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:49:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:49:39 GMT
CMD []
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0227df4100f67814d05f04e139a5e9dca37299fd9d096c7574e16fe632211d4`  
		Last Modified: Thu, 23 Apr 2020 17:14:37 GMT  
		Size: 3.2 MB (3160940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2483e804c9900710b0cfa9c5cad284336a14d95ec28dc1049dc1b3cc10de4`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e906e300d3ad75b25c6513f466d68c5a2dc89ce9663dd6526821b9994ceef549`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1dd819080e27b055eaa67e449dc1475fa02b89c7eb8406d4fd558c817df9ea`  
		Last Modified: Wed, 06 May 2020 00:50:04 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f998921d365053bf7e3f98794f6c23ca44e6809832d78105bc4d2da6bb8521ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67003102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220c6648aa1a61c12d4f11dd3c99b4385828e8c4d9823a5656f4f40294c1d41`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 24 Apr 2020 02:04:18 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 24 Apr 2020 02:04:18 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 24 Apr 2020 02:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:57:36 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:57:37 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:57:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:57:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:57:39 GMT
CMD []
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bec2c432e5c5b4a7f698ed4b9ae252a67bf63604d41a06f871228065ded28a0`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 2.8 MB (2824842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75c0882dce0c322a151afe082f0005164734b3df8b685891a1796351c2c8155`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53c8f90da7135b8a7bd1382287287fc0a77f5671a336d4e82b2d9bd7bfee975`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd7687b9e4e3e2a29a9e10fda7c4e188a5f92507110c037afc83048a374ebb7`  
		Last Modified: Wed, 06 May 2020 00:58:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4f02c4ad7f9483dee2ebc9efe3c66633691504e4c3734fa38b657bb6beb22047
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66714139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c275ab420e15e0f0d3fe6e88b30424974332da758bf2804e204b73dc7a3ddb7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:43:16 GMT
ENV DOCKER_VERSION=19.03.14
# Fri, 11 Dec 2020 03:43:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:43:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:43:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:43:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:43:33 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:43:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 11 Dec 2020 03:43:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 11 Dec 2020 03:43:52 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Fri, 11 Dec 2020 03:43:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 11 Dec 2020 03:43:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:59 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Dec 2020 03:44:01 GMT
EXPOSE 2375 2376
# Fri, 11 Dec 2020 03:44:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Dec 2020 03:44:05 GMT
CMD []
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44406ea375713a15815e70d9f67caccd9d24e3edb888eb33765a7855947a57dd`  
		Last Modified: Fri, 11 Dec 2020 03:46:07 GMT  
		Size: 56.0 MB (55992945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9e082087083b4fa5ee2804222088c41668d42a3cda42a0358add93cfbfed2`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11a145516582d37d1ac882ec6ced4d65ad928b3f5923c73b16211995c42da6`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961068b01d86e33d4e09c9fa6829e3ff7bdb7d3b6a60449681cdf49519058265`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52bcec35351af8539981ca3f0097a0d3b02517a030e2fd5e2c52cd30c72ad66`  
		Last Modified: Fri, 11 Dec 2020 03:46:19 GMT  
		Size: 5.9 MB (5946714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba61fc8445e0471f06d03123c54a76ac7d5d292c0f9983e7021df62400b2d1`  
		Last Modified: Fri, 11 Dec 2020 03:46:19 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28426d0cbfd272b6cb9a64a8b6a1a41033edeae5823a4a809d71f5c1435d7a4`  
		Last Modified: Fri, 11 Dec 2020 03:46:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1827aa166b927762754e480784c7ca687bf2acf61142c2a4e9667cf203a63614`  
		Last Modified: Fri, 11 Dec 2020 03:46:18 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind-rootless`

```console
$ docker pull docker@sha256:4040c071ccf3194453d8a5a753138c9b0e630ec261eaa5824828003e543250a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9ba6316c30560f8bfe973dce6f98709ab80a9333d4b20052950886de63cd673e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94208872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101be3479271665acafd3f369c3299037cadf6459f5d39f628893d2137351897`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
# Wed, 02 Dec 2020 01:46:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 02 Dec 2020 01:46:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 02 Dec 2020 01:46:52 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Wed, 02 Dec 2020 01:46:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 02 Dec 2020 01:46:53 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:54 GMT
VOLUME [/var/lib/docker]
# Wed, 02 Dec 2020 01:46:54 GMT
EXPOSE 2375 2376
# Wed, 02 Dec 2020 01:46:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:54 GMT
CMD []
# Wed, 02 Dec 2020 01:46:59 GMT
RUN apk add --no-cache iproute2
# Wed, 02 Dec 2020 01:47:00 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 02 Dec 2020 01:47:01 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 02 Dec 2020 01:47:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 02 Dec 2020 01:47:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 02 Dec 2020 01:47:05 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 02 Dec 2020 01:47:05 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec33e9a5dc986ed79c57562e16a160920e60a9045ad42b230c8b3c3c2500937`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 6.0 MB (5958689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f95e189f660a26dc7fef2e6cb0cb97e5fd58a2cc3d94401ec05ec021b5d88ec`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48132e2f3ac7e59ba71722801162920cf61f245698f60bf839dc424199bbfceb`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b4df673d204888097abe33a208c939806155dbd1b8e08ea0f23b7dee721183`  
		Last Modified: Wed, 02 Dec 2020 01:47:58 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b03ba64d7c79a3d1f862fe193765409f18ac16cc1b4d4574f25aa288a620296`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 1.1 MB (1092667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a006bc1e4e45e127971d77406f42aa0f538d329e88f95cfcff4b98abfdff2`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72211050ba3a0bd00e3a30db426b705249187eb5609f9f04b32789a2da46e5b`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a296f7783428cadcd8002da2013caaa0ca3ba2832c0b43f34977f2d654d6df6c`  
		Last Modified: Wed, 02 Dec 2020 01:48:11 GMT  
		Size: 19.4 MB (19422676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1110d8f13201e4039f28a0fbf83803b3c25b6fc2ee8fed96a15d2dc02f9b12ba`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-git`

```console
$ docker pull docker@sha256:cb518f3c45dcd4b6c2dec1f45c373e91dadde5c7d74457c58ec6b8fa2d593ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-git` - linux; amd64

```console
$ docker pull docker@sha256:3d7b7d06b06d4df7065f87a398737b006c55c1e789ea3fcbb1608f71f2f01e14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76040588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ed80ea9a6afb9549bdc68ddadd437dbd168ea952021a7a93e00f778f5dab00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
# Wed, 02 Dec 2020 01:47:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82826517bd937097d06a68b9e1bb91a60326d66a9e9071af3db93843edf4c0a2`  
		Last Modified: Wed, 02 Dec 2020 01:48:21 GMT  
		Size: 8.3 MB (8312086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc0b0d405c1e2c6b365d09246756d2d4df5863ead71ff37cde0395e18832b525
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72273342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124c69c34b8489345075587336e4f61de4c56072dd09e3f5d4a9ba6d2f9f4f5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:45 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7cb0ba4509eedc92c81006ddcf0e45d6676a0750dc0867dec331c7d6feb44`  
		Last Modified: Thu, 23 Apr 2020 17:14:54 GMT  
		Size: 7.8 MB (7797688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:e89d2f422796bb472a3f6c301076f8f64fb9f6c3078ff96a8cc7918121a9130f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71205027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba101ef968406449d45b9bf5373293c6f08f400cea9e947b6158777032233591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b175115645c91b877c5783ddd6faf72ccddb1584eabd8187f8f8def8c2e17`  
		Last Modified: Fri, 24 Apr 2020 02:05:44 GMT  
		Size: 7.0 MB (7031330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31c852882a88e4c35ea2f1802f10d116fccbbe7101071d921c12e15beedd4cc4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69266142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae9478277bd44d0819627464380f1048579954877b0e7645ac34d954b63ab20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:43:16 GMT
ENV DOCKER_VERSION=19.03.14
# Fri, 11 Dec 2020 03:43:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:43:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:43:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:43:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:43:33 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:44:19 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44406ea375713a15815e70d9f67caccd9d24e3edb888eb33765a7855947a57dd`  
		Last Modified: Fri, 11 Dec 2020 03:46:07 GMT  
		Size: 56.0 MB (55992945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9e082087083b4fa5ee2804222088c41668d42a3cda42a0358add93cfbfed2`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11a145516582d37d1ac882ec6ced4d65ad928b3f5923c73b16211995c42da6`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961068b01d86e33d4e09c9fa6829e3ff7bdb7d3b6a60449681cdf49519058265`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72293c133127a3af2438e9fdec9f0453dd61056d294aec4c7c40b00a74c2e110`  
		Last Modified: Fri, 11 Dec 2020 03:46:31 GMT  
		Size: 8.5 MB (8503472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind`

```console
$ docker pull docker@sha256:8a1e6994b4b3f94056a49c85da69bf4480e27814a9c6121b196f9f0802b05ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-dind` - linux; amd64

```console
$ docker pull docker@sha256:2a7e15ecad4d18a6bb71b1b828dc7bb1b1a6c890e7420a89726a0649e94e8fb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73691917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f19136cf89d49aee8fa560eaab20e034c6ee17bbce55a9d33e1fbe5baa35b03`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
# Wed, 02 Dec 2020 01:46:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 02 Dec 2020 01:46:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 02 Dec 2020 01:46:52 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Wed, 02 Dec 2020 01:46:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 02 Dec 2020 01:46:53 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:54 GMT
VOLUME [/var/lib/docker]
# Wed, 02 Dec 2020 01:46:54 GMT
EXPOSE 2375 2376
# Wed, 02 Dec 2020 01:46:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:54 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec33e9a5dc986ed79c57562e16a160920e60a9045ad42b230c8b3c3c2500937`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 6.0 MB (5958689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f95e189f660a26dc7fef2e6cb0cb97e5fd58a2cc3d94401ec05ec021b5d88ec`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48132e2f3ac7e59ba71722801162920cf61f245698f60bf839dc424199bbfceb`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b4df673d204888097abe33a208c939806155dbd1b8e08ea0f23b7dee721183`  
		Last Modified: Wed, 02 Dec 2020 01:47:58 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6b0193cbf4d3c304f3bf6c6c253d88c25a22c6ffe6847fd57a6269e4324745f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a37c38067d51b4185a04675f81f45209b82449ce8bbbec68b31d639ba45cd5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 23 Apr 2020 17:13:24 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 23 Apr 2020 17:13:25 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 23 Apr 2020 17:13:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:49:37 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:49:38 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:49:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:49:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:49:39 GMT
CMD []
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0227df4100f67814d05f04e139a5e9dca37299fd9d096c7574e16fe632211d4`  
		Last Modified: Thu, 23 Apr 2020 17:14:37 GMT  
		Size: 3.2 MB (3160940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2483e804c9900710b0cfa9c5cad284336a14d95ec28dc1049dc1b3cc10de4`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e906e300d3ad75b25c6513f466d68c5a2dc89ce9663dd6526821b9994ceef549`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1dd819080e27b055eaa67e449dc1475fa02b89c7eb8406d4fd558c817df9ea`  
		Last Modified: Wed, 06 May 2020 00:50:04 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f998921d365053bf7e3f98794f6c23ca44e6809832d78105bc4d2da6bb8521ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67003102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220c6648aa1a61c12d4f11dd3c99b4385828e8c4d9823a5656f4f40294c1d41`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 24 Apr 2020 02:04:18 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 24 Apr 2020 02:04:18 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 24 Apr 2020 02:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:57:36 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:57:37 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:57:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:57:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:57:39 GMT
CMD []
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bec2c432e5c5b4a7f698ed4b9ae252a67bf63604d41a06f871228065ded28a0`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 2.8 MB (2824842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75c0882dce0c322a151afe082f0005164734b3df8b685891a1796351c2c8155`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53c8f90da7135b8a7bd1382287287fc0a77f5671a336d4e82b2d9bd7bfee975`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd7687b9e4e3e2a29a9e10fda7c4e188a5f92507110c037afc83048a374ebb7`  
		Last Modified: Wed, 06 May 2020 00:58:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4f02c4ad7f9483dee2ebc9efe3c66633691504e4c3734fa38b657bb6beb22047
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66714139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c275ab420e15e0f0d3fe6e88b30424974332da758bf2804e204b73dc7a3ddb7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:43:16 GMT
ENV DOCKER_VERSION=19.03.14
# Fri, 11 Dec 2020 03:43:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:43:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:43:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:43:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:43:33 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:43:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 11 Dec 2020 03:43:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 11 Dec 2020 03:43:52 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Fri, 11 Dec 2020 03:43:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 11 Dec 2020 03:43:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:59 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Dec 2020 03:44:01 GMT
EXPOSE 2375 2376
# Fri, 11 Dec 2020 03:44:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Dec 2020 03:44:05 GMT
CMD []
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44406ea375713a15815e70d9f67caccd9d24e3edb888eb33765a7855947a57dd`  
		Last Modified: Fri, 11 Dec 2020 03:46:07 GMT  
		Size: 56.0 MB (55992945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9e082087083b4fa5ee2804222088c41668d42a3cda42a0358add93cfbfed2`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11a145516582d37d1ac882ec6ced4d65ad928b3f5923c73b16211995c42da6`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961068b01d86e33d4e09c9fa6829e3ff7bdb7d3b6a60449681cdf49519058265`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52bcec35351af8539981ca3f0097a0d3b02517a030e2fd5e2c52cd30c72ad66`  
		Last Modified: Fri, 11 Dec 2020 03:46:19 GMT  
		Size: 5.9 MB (5946714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba61fc8445e0471f06d03123c54a76ac7d5d292c0f9983e7021df62400b2d1`  
		Last Modified: Fri, 11 Dec 2020 03:46:19 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28426d0cbfd272b6cb9a64a8b6a1a41033edeae5823a4a809d71f5c1435d7a4`  
		Last Modified: Fri, 11 Dec 2020 03:46:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1827aa166b927762754e480784c7ca687bf2acf61142c2a4e9667cf203a63614`  
		Last Modified: Fri, 11 Dec 2020 03:46:18 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind-rootless`

```console
$ docker pull docker@sha256:4040c071ccf3194453d8a5a753138c9b0e630ec261eaa5824828003e543250a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9ba6316c30560f8bfe973dce6f98709ab80a9333d4b20052950886de63cd673e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94208872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101be3479271665acafd3f369c3299037cadf6459f5d39f628893d2137351897`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
# Wed, 02 Dec 2020 01:46:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 02 Dec 2020 01:46:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 02 Dec 2020 01:46:52 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Wed, 02 Dec 2020 01:46:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 02 Dec 2020 01:46:53 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:54 GMT
VOLUME [/var/lib/docker]
# Wed, 02 Dec 2020 01:46:54 GMT
EXPOSE 2375 2376
# Wed, 02 Dec 2020 01:46:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:54 GMT
CMD []
# Wed, 02 Dec 2020 01:46:59 GMT
RUN apk add --no-cache iproute2
# Wed, 02 Dec 2020 01:47:00 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 02 Dec 2020 01:47:01 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 02 Dec 2020 01:47:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 02 Dec 2020 01:47:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 02 Dec 2020 01:47:05 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 02 Dec 2020 01:47:05 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec33e9a5dc986ed79c57562e16a160920e60a9045ad42b230c8b3c3c2500937`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 6.0 MB (5958689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f95e189f660a26dc7fef2e6cb0cb97e5fd58a2cc3d94401ec05ec021b5d88ec`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48132e2f3ac7e59ba71722801162920cf61f245698f60bf839dc424199bbfceb`  
		Last Modified: Wed, 02 Dec 2020 01:47:59 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b4df673d204888097abe33a208c939806155dbd1b8e08ea0f23b7dee721183`  
		Last Modified: Wed, 02 Dec 2020 01:47:58 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b03ba64d7c79a3d1f862fe193765409f18ac16cc1b4d4574f25aa288a620296`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 1.1 MB (1092667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a006bc1e4e45e127971d77406f42aa0f538d329e88f95cfcff4b98abfdff2`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72211050ba3a0bd00e3a30db426b705249187eb5609f9f04b32789a2da46e5b`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a296f7783428cadcd8002da2013caaa0ca3ba2832c0b43f34977f2d654d6df6c`  
		Last Modified: Wed, 02 Dec 2020 01:48:11 GMT  
		Size: 19.4 MB (19422676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1110d8f13201e4039f28a0fbf83803b3c25b6fc2ee8fed96a15d2dc02f9b12ba`  
		Last Modified: Wed, 02 Dec 2020 01:48:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-git`

```console
$ docker pull docker@sha256:cb518f3c45dcd4b6c2dec1f45c373e91dadde5c7d74457c58ec6b8fa2d593ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-git` - linux; amd64

```console
$ docker pull docker@sha256:3d7b7d06b06d4df7065f87a398737b006c55c1e789ea3fcbb1608f71f2f01e14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76040588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ed80ea9a6afb9549bdc68ddadd437dbd168ea952021a7a93e00f778f5dab00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 02 Dec 2020 01:46:37 GMT
ENV DOCKER_VERSION=19.03.14
# Wed, 02 Dec 2020 01:46:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 02 Dec 2020 01:46:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 02 Dec 2020 01:46:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 02 Dec 2020 01:46:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 02 Dec 2020 01:46:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:46:44 GMT
CMD ["sh"]
# Wed, 02 Dec 2020 01:47:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef`  
		Last Modified: Wed, 02 Dec 2020 01:47:47 GMT  
		Size: 62.9 MB (62890748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946`  
		Last Modified: Wed, 02 Dec 2020 01:47:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e`  
		Last Modified: Wed, 02 Dec 2020 01:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82826517bd937097d06a68b9e1bb91a60326d66a9e9071af3db93843edf4c0a2`  
		Last Modified: Wed, 02 Dec 2020 01:48:21 GMT  
		Size: 8.3 MB (8312086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc0b0d405c1e2c6b365d09246756d2d4df5863ead71ff37cde0395e18832b525
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72273342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124c69c34b8489345075587336e4f61de4c56072dd09e3f5d4a9ba6d2f9f4f5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:45 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7cb0ba4509eedc92c81006ddcf0e45d6676a0750dc0867dec331c7d6feb44`  
		Last Modified: Thu, 23 Apr 2020 17:14:54 GMT  
		Size: 7.8 MB (7797688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:e89d2f422796bb472a3f6c301076f8f64fb9f6c3078ff96a8cc7918121a9130f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71205027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba101ef968406449d45b9bf5373293c6f08f400cea9e947b6158777032233591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b175115645c91b877c5783ddd6faf72ccddb1584eabd8187f8f8def8c2e17`  
		Last Modified: Fri, 24 Apr 2020 02:05:44 GMT  
		Size: 7.0 MB (7031330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31c852882a88e4c35ea2f1802f10d116fccbbe7101071d921c12e15beedd4cc4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69266142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae9478277bd44d0819627464380f1048579954877b0e7645ac34d954b63ab20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:43:16 GMT
ENV DOCKER_VERSION=19.03.14
# Fri, 11 Dec 2020 03:43:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:43:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:43:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:43:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:43:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:43:33 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:44:19 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44406ea375713a15815e70d9f67caccd9d24e3edb888eb33765a7855947a57dd`  
		Last Modified: Fri, 11 Dec 2020 03:46:07 GMT  
		Size: 56.0 MB (55992945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9e082087083b4fa5ee2804222088c41668d42a3cda42a0358add93cfbfed2`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11a145516582d37d1ac882ec6ced4d65ad928b3f5923c73b16211995c42da6`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961068b01d86e33d4e09c9fa6829e3ff7bdb7d3b6a60449681cdf49519058265`  
		Last Modified: Fri, 11 Dec 2020 03:45:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72293c133127a3af2438e9fdec9f0453dd61056d294aec4c7c40b00a74c2e110`  
		Last Modified: Fri, 11 Dec 2020 03:46:31 GMT  
		Size: 8.5 MB (8503472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20`

```console
$ docker pull docker@sha256:6e4375a0d68ebd4de32d42b3e23bfaffff328c1a1c6d860689e7931c3536d77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:3715824e5f0233384f4bc6e0cc9731b24ecfc635beaa2f5499c04f29ee2d7c50
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c48ffa8038e009a8fdab7f3f369b40cb3f505cdf130aeb0b3442fa6b3c1c2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f65a8021b3332e2cfe3498c23cf10ccd0010db66f6f0bc1fb65dff8d280b9ab8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68327992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaf43b927733dcfd7b87c5a733c444df7c3d364e065dbebfdc2271d9caaa502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:6e4375a0d68ebd4de32d42b3e23bfaffff328c1a1c6d860689e7931c3536d77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:3715824e5f0233384f4bc6e0cc9731b24ecfc635beaa2f5499c04f29ee2d7c50
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c48ffa8038e009a8fdab7f3f369b40cb3f505cdf130aeb0b3442fa6b3c1c2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f65a8021b3332e2cfe3498c23cf10ccd0010db66f6f0bc1fb65dff8d280b9ab8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68327992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaf43b927733dcfd7b87c5a733c444df7c3d364e065dbebfdc2271d9caaa502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.0`

```console
$ docker pull docker@sha256:6e4375a0d68ebd4de32d42b3e23bfaffff328c1a1c6d860689e7931c3536d77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.0` - linux; amd64

```console
$ docker pull docker@sha256:3715824e5f0233384f4bc6e0cc9731b24ecfc635beaa2f5499c04f29ee2d7c50
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c48ffa8038e009a8fdab7f3f369b40cb3f505cdf130aeb0b3442fa6b3c1c2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f65a8021b3332e2cfe3498c23cf10ccd0010db66f6f0bc1fb65dff8d280b9ab8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68327992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaf43b927733dcfd7b87c5a733c444df7c3d364e065dbebfdc2271d9caaa502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.0-dind`

```console
$ docker pull docker@sha256:aa21e6cb69a8a8a8eb088831ac1256f495d9d3d819c9d8272fb96cd270cd5311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:e3fce5a4c98c04f4a87ff99f8685a7786c7e6f56dbf8fe84361d18243c3e3dc1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80259056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4603edb9dd6d085df3c3316b52823a8bd3a8ecee36596b57cd555b1daee12`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8158787e039990a61d9311c7dff1f5fd1f1dfd45598d300c5e0256f7e56826b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74279455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7571c75fa44d208540d36f7841820f114c5fbbd34d59040cbb3514898a2bc3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:42:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 11 Dec 2020 03:42:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 11 Dec 2020 03:42:49 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Fri, 11 Dec 2020 03:42:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 11 Dec 2020 03:42:54 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:55 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Dec 2020 03:42:55 GMT
EXPOSE 2375 2376
# Fri, 11 Dec 2020 03:42:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:57 GMT
CMD []
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3c1e6f870afdbfa36d1f6b8b5862e09bd24e7347e31d6ecd63594c5ef89189`  
		Last Modified: Fri, 11 Dec 2020 03:45:24 GMT  
		Size: 5.9 MB (5946711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0d66fa871f6f8fe3a50e5335baf2447609e1155d7e45ba8d39b57cbe03bb52`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9696c35219b6de77caadcd8eec2cd44092725ee74b071fd3cb957b8f813cb147`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcba874525fb94f3a6ab2d404a63b18856698968e79bdb2648814d11989235e`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.0-dind-rootless`

```console
$ docker pull docker@sha256:140d629d80a53ee558d442d6e6425fcae76c687b0a910262af867b0a9ad1fc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:20.10.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a433dd7b2f9cd8b8e5fc4655b675584cce9f712da996c6f46165d8495efbc69f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101524712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4b3576648314bb2a5af93388a92239da8e49f71c9a73477ac9ddb51b4b3c90`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
# Thu, 10 Dec 2020 16:34:30 GMT
RUN apk add --no-cache iproute2
# Thu, 10 Dec 2020 16:34:31 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 10 Dec 2020 16:34:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 10 Dec 2020 16:34:35 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 10 Dec 2020 16:34:35 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 10 Dec 2020 16:34:35 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9134a376d14301f855d03ff3808689d77e7b85cea7ab8213478ab7ca7d8789c`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 1.1 MB (1092671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63fd1383e6fbafd721d12e0c99aea5120a31aa52aefb5aa1808a41ffadb9`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772148c137c8bd1474c6946b0192b3f7a786c997d26b80affcb79d17444eff62`  
		Last Modified: Thu, 10 Dec 2020 16:35:40 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c5ac8ed7ead1c35040d0bb2392053119d1646b27dae4a766925ebaa248f388`  
		Last Modified: Thu, 10 Dec 2020 16:35:45 GMT  
		Size: 20.2 MB (20171371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ddf2da86992920ab4482bf8a52843988196d895f07619d775f4f1258a50cc0`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.0-git`

```console
$ docker pull docker@sha256:ded3e2486106ef8fcd68966e3c377359f6c8e3f62baba7864aa716b54fc8461b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.0-git` - linux; amd64

```console
$ docker pull docker@sha256:963d6c07001b3962f55fe56f0cf7cd6f5d306df5a7f227151dc16cb06c35cf22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82607710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97934d62ad5b08664cbaba064d8db6a9aea11adda2cb7004c4fc28730f8be4ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:41 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d82cf2a24239a6d53ce460695ca5978f5cfd5d682d585170e2f0041c200ade`  
		Last Modified: Thu, 10 Dec 2020 16:36:02 GMT  
		Size: 8.3 MB (8312115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.0-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:836a38373d532ac55e66096590e2d8c7b4833cf0cfabd80c0f004d050080a74c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76831460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961e0b3d34ce5f4ae39dcadff0006d5afcddf128492dfb2da665a0fb5c0d3ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:43:08 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99c483ed624af2276f16b538d32a3eec95bb4309d636878022d76d74bae9def`  
		Last Modified: Fri, 11 Dec 2020 03:45:39 GMT  
		Size: 8.5 MB (8503468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:aa21e6cb69a8a8a8eb088831ac1256f495d9d3d819c9d8272fb96cd270cd5311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:e3fce5a4c98c04f4a87ff99f8685a7786c7e6f56dbf8fe84361d18243c3e3dc1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80259056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4603edb9dd6d085df3c3316b52823a8bd3a8ecee36596b57cd555b1daee12`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8158787e039990a61d9311c7dff1f5fd1f1dfd45598d300c5e0256f7e56826b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74279455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7571c75fa44d208540d36f7841820f114c5fbbd34d59040cbb3514898a2bc3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:42:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 11 Dec 2020 03:42:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 11 Dec 2020 03:42:49 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Fri, 11 Dec 2020 03:42:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 11 Dec 2020 03:42:54 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:55 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Dec 2020 03:42:55 GMT
EXPOSE 2375 2376
# Fri, 11 Dec 2020 03:42:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:57 GMT
CMD []
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3c1e6f870afdbfa36d1f6b8b5862e09bd24e7347e31d6ecd63594c5ef89189`  
		Last Modified: Fri, 11 Dec 2020 03:45:24 GMT  
		Size: 5.9 MB (5946711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0d66fa871f6f8fe3a50e5335baf2447609e1155d7e45ba8d39b57cbe03bb52`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9696c35219b6de77caadcd8eec2cd44092725ee74b071fd3cb957b8f813cb147`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcba874525fb94f3a6ab2d404a63b18856698968e79bdb2648814d11989235e`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:140d629d80a53ee558d442d6e6425fcae76c687b0a910262af867b0a9ad1fc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a433dd7b2f9cd8b8e5fc4655b675584cce9f712da996c6f46165d8495efbc69f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101524712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4b3576648314bb2a5af93388a92239da8e49f71c9a73477ac9ddb51b4b3c90`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
# Thu, 10 Dec 2020 16:34:30 GMT
RUN apk add --no-cache iproute2
# Thu, 10 Dec 2020 16:34:31 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 10 Dec 2020 16:34:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 10 Dec 2020 16:34:35 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 10 Dec 2020 16:34:35 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 10 Dec 2020 16:34:35 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9134a376d14301f855d03ff3808689d77e7b85cea7ab8213478ab7ca7d8789c`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 1.1 MB (1092671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63fd1383e6fbafd721d12e0c99aea5120a31aa52aefb5aa1808a41ffadb9`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772148c137c8bd1474c6946b0192b3f7a786c997d26b80affcb79d17444eff62`  
		Last Modified: Thu, 10 Dec 2020 16:35:40 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c5ac8ed7ead1c35040d0bb2392053119d1646b27dae4a766925ebaa248f388`  
		Last Modified: Thu, 10 Dec 2020 16:35:45 GMT  
		Size: 20.2 MB (20171371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ddf2da86992920ab4482bf8a52843988196d895f07619d775f4f1258a50cc0`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:ded3e2486106ef8fcd68966e3c377359f6c8e3f62baba7864aa716b54fc8461b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:963d6c07001b3962f55fe56f0cf7cd6f5d306df5a7f227151dc16cb06c35cf22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82607710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97934d62ad5b08664cbaba064d8db6a9aea11adda2cb7004c4fc28730f8be4ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:41 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d82cf2a24239a6d53ce460695ca5978f5cfd5d682d585170e2f0041c200ade`  
		Last Modified: Thu, 10 Dec 2020 16:36:02 GMT  
		Size: 8.3 MB (8312115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:836a38373d532ac55e66096590e2d8c7b4833cf0cfabd80c0f004d050080a74c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76831460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961e0b3d34ce5f4ae39dcadff0006d5afcddf128492dfb2da665a0fb5c0d3ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:43:08 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99c483ed624af2276f16b538d32a3eec95bb4309d636878022d76d74bae9def`  
		Last Modified: Fri, 11 Dec 2020 03:45:39 GMT  
		Size: 8.5 MB (8503468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:aa21e6cb69a8a8a8eb088831ac1256f495d9d3d819c9d8272fb96cd270cd5311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:e3fce5a4c98c04f4a87ff99f8685a7786c7e6f56dbf8fe84361d18243c3e3dc1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80259056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4603edb9dd6d085df3c3316b52823a8bd3a8ecee36596b57cd555b1daee12`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8158787e039990a61d9311c7dff1f5fd1f1dfd45598d300c5e0256f7e56826b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74279455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7571c75fa44d208540d36f7841820f114c5fbbd34d59040cbb3514898a2bc3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:42:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 11 Dec 2020 03:42:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 11 Dec 2020 03:42:49 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Fri, 11 Dec 2020 03:42:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 11 Dec 2020 03:42:54 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:55 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Dec 2020 03:42:55 GMT
EXPOSE 2375 2376
# Fri, 11 Dec 2020 03:42:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:57 GMT
CMD []
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3c1e6f870afdbfa36d1f6b8b5862e09bd24e7347e31d6ecd63594c5ef89189`  
		Last Modified: Fri, 11 Dec 2020 03:45:24 GMT  
		Size: 5.9 MB (5946711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0d66fa871f6f8fe3a50e5335baf2447609e1155d7e45ba8d39b57cbe03bb52`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9696c35219b6de77caadcd8eec2cd44092725ee74b071fd3cb957b8f813cb147`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcba874525fb94f3a6ab2d404a63b18856698968e79bdb2648814d11989235e`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:140d629d80a53ee558d442d6e6425fcae76c687b0a910262af867b0a9ad1fc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a433dd7b2f9cd8b8e5fc4655b675584cce9f712da996c6f46165d8495efbc69f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101524712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4b3576648314bb2a5af93388a92239da8e49f71c9a73477ac9ddb51b4b3c90`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
# Thu, 10 Dec 2020 16:34:30 GMT
RUN apk add --no-cache iproute2
# Thu, 10 Dec 2020 16:34:31 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 10 Dec 2020 16:34:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 10 Dec 2020 16:34:35 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 10 Dec 2020 16:34:35 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 10 Dec 2020 16:34:35 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9134a376d14301f855d03ff3808689d77e7b85cea7ab8213478ab7ca7d8789c`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 1.1 MB (1092671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63fd1383e6fbafd721d12e0c99aea5120a31aa52aefb5aa1808a41ffadb9`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772148c137c8bd1474c6946b0192b3f7a786c997d26b80affcb79d17444eff62`  
		Last Modified: Thu, 10 Dec 2020 16:35:40 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c5ac8ed7ead1c35040d0bb2392053119d1646b27dae4a766925ebaa248f388`  
		Last Modified: Thu, 10 Dec 2020 16:35:45 GMT  
		Size: 20.2 MB (20171371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ddf2da86992920ab4482bf8a52843988196d895f07619d775f4f1258a50cc0`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:ded3e2486106ef8fcd68966e3c377359f6c8e3f62baba7864aa716b54fc8461b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:963d6c07001b3962f55fe56f0cf7cd6f5d306df5a7f227151dc16cb06c35cf22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82607710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97934d62ad5b08664cbaba064d8db6a9aea11adda2cb7004c4fc28730f8be4ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:41 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d82cf2a24239a6d53ce460695ca5978f5cfd5d682d585170e2f0041c200ade`  
		Last Modified: Thu, 10 Dec 2020 16:36:02 GMT  
		Size: 8.3 MB (8312115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:836a38373d532ac55e66096590e2d8c7b4833cf0cfabd80c0f004d050080a74c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76831460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961e0b3d34ce5f4ae39dcadff0006d5afcddf128492dfb2da665a0fb5c0d3ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:43:08 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99c483ed624af2276f16b538d32a3eec95bb4309d636878022d76d74bae9def`  
		Last Modified: Fri, 11 Dec 2020 03:45:39 GMT  
		Size: 8.5 MB (8503468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:3759984ac1964d5ef82d0f791427bfcddcdde1f729c384f46b3c2db00229f7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:e3fce5a4c98c04f4a87ff99f8685a7786c7e6f56dbf8fe84361d18243c3e3dc1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80259056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4603edb9dd6d085df3c3316b52823a8bd3a8ecee36596b57cd555b1daee12`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6b0193cbf4d3c304f3bf6c6c253d88c25a22c6ffe6847fd57a6269e4324745f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a37c38067d51b4185a04675f81f45209b82449ce8bbbec68b31d639ba45cd5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 23 Apr 2020 17:13:24 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 23 Apr 2020 17:13:25 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 23 Apr 2020 17:13:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:49:37 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:49:38 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:49:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:49:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:49:39 GMT
CMD []
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0227df4100f67814d05f04e139a5e9dca37299fd9d096c7574e16fe632211d4`  
		Last Modified: Thu, 23 Apr 2020 17:14:37 GMT  
		Size: 3.2 MB (3160940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2483e804c9900710b0cfa9c5cad284336a14d95ec28dc1049dc1b3cc10de4`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e906e300d3ad75b25c6513f466d68c5a2dc89ce9663dd6526821b9994ceef549`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1dd819080e27b055eaa67e449dc1475fa02b89c7eb8406d4fd558c817df9ea`  
		Last Modified: Wed, 06 May 2020 00:50:04 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f998921d365053bf7e3f98794f6c23ca44e6809832d78105bc4d2da6bb8521ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67003102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220c6648aa1a61c12d4f11dd3c99b4385828e8c4d9823a5656f4f40294c1d41`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 24 Apr 2020 02:04:18 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 24 Apr 2020 02:04:18 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 24 Apr 2020 02:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:57:36 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:57:37 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:57:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:57:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:57:39 GMT
CMD []
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bec2c432e5c5b4a7f698ed4b9ae252a67bf63604d41a06f871228065ded28a0`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 2.8 MB (2824842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75c0882dce0c322a151afe082f0005164734b3df8b685891a1796351c2c8155`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53c8f90da7135b8a7bd1382287287fc0a77f5671a336d4e82b2d9bd7bfee975`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd7687b9e4e3e2a29a9e10fda7c4e188a5f92507110c037afc83048a374ebb7`  
		Last Modified: Wed, 06 May 2020 00:58:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8158787e039990a61d9311c7dff1f5fd1f1dfd45598d300c5e0256f7e56826b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74279455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7571c75fa44d208540d36f7841820f114c5fbbd34d59040cbb3514898a2bc3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:42:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 11 Dec 2020 03:42:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 11 Dec 2020 03:42:49 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Fri, 11 Dec 2020 03:42:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 11 Dec 2020 03:42:54 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:55 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Dec 2020 03:42:55 GMT
EXPOSE 2375 2376
# Fri, 11 Dec 2020 03:42:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:57 GMT
CMD []
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3c1e6f870afdbfa36d1f6b8b5862e09bd24e7347e31d6ecd63594c5ef89189`  
		Last Modified: Fri, 11 Dec 2020 03:45:24 GMT  
		Size: 5.9 MB (5946711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0d66fa871f6f8fe3a50e5335baf2447609e1155d7e45ba8d39b57cbe03bb52`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9696c35219b6de77caadcd8eec2cd44092725ee74b071fd3cb957b8f813cb147`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcba874525fb94f3a6ab2d404a63b18856698968e79bdb2648814d11989235e`  
		Last Modified: Fri, 11 Dec 2020 03:45:22 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:140d629d80a53ee558d442d6e6425fcae76c687b0a910262af867b0a9ad1fc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a433dd7b2f9cd8b8e5fc4655b675584cce9f712da996c6f46165d8495efbc69f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101524712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4b3576648314bb2a5af93388a92239da8e49f71c9a73477ac9ddb51b4b3c90`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
# Thu, 10 Dec 2020 16:34:30 GMT
RUN apk add --no-cache iproute2
# Thu, 10 Dec 2020 16:34:31 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 10 Dec 2020 16:34:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 10 Dec 2020 16:34:35 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 10 Dec 2020 16:34:35 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 10 Dec 2020 16:34:35 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9134a376d14301f855d03ff3808689d77e7b85cea7ab8213478ab7ca7d8789c`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 1.1 MB (1092671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63fd1383e6fbafd721d12e0c99aea5120a31aa52aefb5aa1808a41ffadb9`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772148c137c8bd1474c6946b0192b3f7a786c997d26b80affcb79d17444eff62`  
		Last Modified: Thu, 10 Dec 2020 16:35:40 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c5ac8ed7ead1c35040d0bb2392053119d1646b27dae4a766925ebaa248f388`  
		Last Modified: Thu, 10 Dec 2020 16:35:45 GMT  
		Size: 20.2 MB (20171371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ddf2da86992920ab4482bf8a52843988196d895f07619d775f4f1258a50cc0`  
		Last Modified: Thu, 10 Dec 2020 16:35:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:5f54351dd06a92bed62bb7188474d032a730b1b00ba75ebe8c7a29e08d5dbb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:963d6c07001b3962f55fe56f0cf7cd6f5d306df5a7f227151dc16cb06c35cf22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82607710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97934d62ad5b08664cbaba064d8db6a9aea11adda2cb7004c4fc28730f8be4ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:41 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d82cf2a24239a6d53ce460695ca5978f5cfd5d682d585170e2f0041c200ade`  
		Last Modified: Thu, 10 Dec 2020 16:36:02 GMT  
		Size: 8.3 MB (8312115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc0b0d405c1e2c6b365d09246756d2d4df5863ead71ff37cde0395e18832b525
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72273342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124c69c34b8489345075587336e4f61de4c56072dd09e3f5d4a9ba6d2f9f4f5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:45 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7cb0ba4509eedc92c81006ddcf0e45d6676a0750dc0867dec331c7d6feb44`  
		Last Modified: Thu, 23 Apr 2020 17:14:54 GMT  
		Size: 7.8 MB (7797688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v7

```console
$ docker pull docker@sha256:e89d2f422796bb472a3f6c301076f8f64fb9f6c3078ff96a8cc7918121a9130f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71205027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba101ef968406449d45b9bf5373293c6f08f400cea9e947b6158777032233591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b175115645c91b877c5783ddd6faf72ccddb1584eabd8187f8f8def8c2e17`  
		Last Modified: Fri, 24 Apr 2020 02:05:44 GMT  
		Size: 7.0 MB (7031330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:836a38373d532ac55e66096590e2d8c7b4833cf0cfabd80c0f004d050080a74c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76831460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961e0b3d34ce5f4ae39dcadff0006d5afcddf128492dfb2da665a0fb5c0d3ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
# Fri, 11 Dec 2020 03:43:08 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99c483ed624af2276f16b538d32a3eec95bb4309d636878022d76d74bae9def`  
		Last Modified: Fri, 11 Dec 2020 03:45:39 GMT  
		Size: 8.5 MB (8503468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:dd934a6a28e572519f9d12740033e4f0807ae337fc05a4e58b47d64f6629e28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:3715824e5f0233384f4bc6e0cc9731b24ecfc635beaa2f5499c04f29ee2d7c50
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c48ffa8038e009a8fdab7f3f369b40cb3f505cdf130aeb0b3442fa6b3c1c2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:18d39b6848cecae067cc0d94c554029bfc88d3069c80bb5049d54da659249b94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3106fcafb44a465ee4e0efadc103e5018d57587bd5d5ba6f465846bf7c3844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce46ea18798c578f8923e0ced4c9996c30363fc35edd1b1c40e5e542407818ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a685736103d7a1e988f52fb20b130a353e545dff4ccd52c9b075d5ead6f11d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f65a8021b3332e2cfe3498c23cf10ccd0010db66f6f0bc1fb65dff8d280b9ab8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68327992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaf43b927733dcfd7b87c5a733c444df7c3d364e065dbebfdc2271d9caaa502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
