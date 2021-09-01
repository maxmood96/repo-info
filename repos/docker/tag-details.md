<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:20`](#docker20)
-	[`docker:20-dind`](#docker20-dind)
-	[`docker:20-dind-rootless`](#docker20-dind-rootless)
-	[`docker:20-git`](#docker20-git)
-	[`docker:20-windowsservercore`](#docker20-windowsservercore)
-	[`docker:20-windowsservercore-1809`](#docker20-windowsservercore-1809)
-	[`docker:20.10`](#docker2010)
-	[`docker:20.10-dind`](#docker2010-dind)
-	[`docker:20.10-dind-rootless`](#docker2010-dind-rootless)
-	[`docker:20.10-git`](#docker2010-git)
-	[`docker:20.10-windowsservercore`](#docker2010-windowsservercore)
-	[`docker:20.10-windowsservercore-1809`](#docker2010-windowsservercore-1809)
-	[`docker:20.10.8`](#docker20108)
-	[`docker:20.10.8-alpine3.14`](#docker20108-alpine314)
-	[`docker:20.10.8-dind`](#docker20108-dind)
-	[`docker:20.10.8-dind-alpine3.14`](#docker20108-dind-alpine314)
-	[`docker:20.10.8-dind-rootless`](#docker20108-dind-rootless)
-	[`docker:20.10.8-git`](#docker20108-git)
-	[`docker:20.10.8-windowsservercore`](#docker20108-windowsservercore)
-	[`docker:20.10.8-windowsservercore-1809`](#docker20108-windowsservercore-1809)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)

## `docker:20`

```console
$ docker pull docker@sha256:cbf25f4f97f8ab21eabc463af9798d733fbb32b3a34483d5ba74b1bff914910c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:35f612c47195c6e7c1e9ecc80c1b1a00402f3c039e768dd08b2ddb237fd5d0ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66151138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67ee0b7de2f5cca0d60fe996f082ee6795d35fdd0c7823325b0f7855f57c342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2fad5f90265a7c9c4ee73f0b0eaa7b5ed8203af4cd0464dda8f7e1f4b28a5ad7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60042992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3734d5adc5ac9557175d6c0acb930e7ed6d75e1f2e52e8c170b4ade3f76806a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:b1b2943cc94fa1b87be7d612656f72f9a6f4132e96d7a5e4e4e35b383c6e3102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:d1c7515d7ba19c572b6f60ec904cf0a875b3bf60c427205845b5ab7b432b05ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72680575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc41137f712d794c3471c40b56f946667cfe729e112ebc6f1a824bcc775f679`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 00:26:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:26:55 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 00:26:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 00:26:57 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:57 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 00:26:57 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 00:26:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:58 GMT
CMD []
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5973cffe69ed6ec4ab2e2a3a191794cfba7339588cdbc4f3c6355e040c05fb`  
		Last Modified: Wed, 01 Sep 2021 00:28:13 GMT  
		Size: 6.5 MB (6524532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a47d00d0a33090100f0be8b5d564e20357fa60a275aba922aea6db6fb47531`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8a29d06b5993e5468f57fa6a9d0adff807919d6c664b785a96b1fb6a96d8`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 978.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6762b64189d2495a0856c3f7d465d7ad0f91a4e2db42b4093e70c7b55e571211`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f21866d81ae3b92303af07fe477794e4e4bf43836de0d41b4c212d4469d41a1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66466448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de95d7c2e2d4cc59123fcfef69442499876a675bb59ab504b9ad78c5881fe85a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:39:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 21:39:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:45 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 21:39:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 21:39:46 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:47 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 21:39:47 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 21:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:47 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff707a384f2d3eeae1ec32f9044142bb5c896541416c18d1bf45142da30ae`  
		Last Modified: Wed, 01 Sep 2021 21:41:30 GMT  
		Size: 6.4 MB (6418561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d94df880147a87f1fba1c3115c37eb4b50c95fc93694f4d5e1fc22f353fd3`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ada35578ff611689fc1c810d1603dd6b6c606175e97737d9f3073f4631235b0`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcd3a1f2fec5765d757040410b3f777d30970931dd552544b55ada1dc9ebe8`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:99a866bf721d434fdda04b68126b8a8611b2f84633ce37c28814cd33ead91de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:33a0761966c87569be2a9763c8c477dd3e8981982c8abc4324c090f9d2478231
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92930272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5357717b590217cbd992209ed6e2fb34e8ba65a74d3a5324c9b916395a15cb1b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 00:26:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:26:55 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 00:26:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 00:26:57 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:57 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 00:26:57 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 00:26:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:58 GMT
CMD []
# Wed, 01 Sep 2021 00:27:03 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 00:27:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 00:27:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:27:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 00:27:07 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 00:27:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 00:27:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5973cffe69ed6ec4ab2e2a3a191794cfba7339588cdbc4f3c6355e040c05fb`  
		Last Modified: Wed, 01 Sep 2021 00:28:13 GMT  
		Size: 6.5 MB (6524532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a47d00d0a33090100f0be8b5d564e20357fa60a275aba922aea6db6fb47531`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8a29d06b5993e5468f57fa6a9d0adff807919d6c664b785a96b1fb6a96d8`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 978.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6762b64189d2495a0856c3f7d465d7ad0f91a4e2db42b4093e70c7b55e571211`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dbc14ca68582d0028413d0826f71ced2423d092126de153c91bbf05e4c98fa`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.1 MB (1131899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2498ce93d923f17fb67004858df28e840d729cf6e6fbdfa82ed3c82679ebe4`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64015873fa22ddcd58c65fa437669d9153f1a1fd72fd3a43dbd6873f129461b9`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcf73021c4287b49de963988902f36818158f72e0ccd6e3b93af6bb3f4e7ef9`  
		Last Modified: Wed, 01 Sep 2021 00:28:39 GMT  
		Size: 19.1 MB (19116093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ea275b05bd4bf7a61d8bc934c3d72b3d30ae866ed920fdd7d0a5d06933c0d`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:01a3353757a17aa2125c2a6181c436134d7a0055df0ef3ba323826350e1d0ff1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88731007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcfee17c3e4c3e92f1ae3c5a77520971a3633eebf269f8a4a895634a5ad06c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:39:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 21:39:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:45 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 21:39:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 21:39:46 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:47 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 21:39:47 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 21:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:47 GMT
CMD []
# Wed, 01 Sep 2021 21:39:55 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 21:39:56 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 21:39:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 21:39:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 21:39:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 21:39:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff707a384f2d3eeae1ec32f9044142bb5c896541416c18d1bf45142da30ae`  
		Last Modified: Wed, 01 Sep 2021 21:41:30 GMT  
		Size: 6.4 MB (6418561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d94df880147a87f1fba1c3115c37eb4b50c95fc93694f4d5e1fc22f353fd3`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ada35578ff611689fc1c810d1603dd6b6c606175e97737d9f3073f4631235b0`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcd3a1f2fec5765d757040410b3f777d30970931dd552544b55ada1dc9ebe8`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0727607c4852e6356bf01e7ea1c0d090e6100e1045cd881eca01515749b53e6`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 1.2 MB (1168111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee229379e57fe13e75a06a3453c3afa2ec3959e936165ad25b24fa00a2bec57`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5c0508be8bb4e91bd2c3895baa8ee248bf3b1bb5bd9d605a8c5da8b4aeff1a`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dc3c7f21a4603739eb746480b3aa01086f70941d2b2141504e7c7e796a1bab`  
		Last Modified: Wed, 01 Sep 2021 21:41:57 GMT  
		Size: 21.1 MB (21094732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da3b6b5f43f82f2e3e8c853aefbe98b52cbd1ff0fc99294851db16ee9eefa2f`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:f830e24b3e166774970348fc36ea0e9d108e908e93f7ba6c6c206f2f12faf758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:709ceab8cd1164fbf0c03b1991f8f412a1543023548fa7a30de2268d399723aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d03657b093bb281e2bf0c19460dbf0f73fbf181780da767109363461960b6de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:27:13 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8c9f33643fb8321012f52f6a1ec572b42b9f29dcd29c0dcf2635ad0c9d1911`  
		Last Modified: Wed, 01 Sep 2021 00:29:00 GMT  
		Size: 6.4 MB (6402499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4951d55d07df56eb3dc8823e5abb438f05ced009af250666aab6381f9ef2a99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66784792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c1f1eae55906bc481ffd709ea71e35a3f9aa3dde59572a62cadf79d7442716`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:40:07 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac87a5e4495fa9d6f260ed353f2f2ed60461d2ccc2fcce309f3a0ab5cfe2a01`  
		Last Modified: Wed, 01 Sep 2021 21:42:18 GMT  
		Size: 6.7 MB (6741800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:81d849a5208118837827efb4f0433db49a305260c37f83ff813590c03521247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `docker:20-windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull docker@sha256:a86536c27f22717fed9d5bcb2ff43eb82f0c2e7eb602d6b9c5d714cd0b706e9a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737269694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594329f431fd456d89c771444f5e662730713ccd58a9d03b52796bd7fa42e35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Aug 2021 23:23:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Aug 2021 23:23:52 GMT
ENV DOCKER_VERSION=20.10.8
# Tue, 24 Aug 2021 23:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.8.zip
# Tue, 24 Aug 2021 23:24:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4896faf56da9e635d1215c12a54c8734e695682b57d6e038ca62fd90b532b`  
		Last Modified: Tue, 24 Aug 2021 23:25:13 GMT  
		Size: 378.4 KB (378370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49ef5983ec79b546f9ba4e76c016df80499c33627052d1101b851ffb7b4fde`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8baf6cf9c02dbd2217455c62d5ee255fd65036a9a442d0d4794abb2fa68c59`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0b72a29873171e2e2cfc43d555ef003e482ffe643396157ba76e4b22ab3017`  
		Last Modified: Tue, 24 Aug 2021 23:26:06 GMT  
		Size: 50.9 MB (50889387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:81d849a5208118837827efb4f0433db49a305260c37f83ff813590c03521247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull docker@sha256:a86536c27f22717fed9d5bcb2ff43eb82f0c2e7eb602d6b9c5d714cd0b706e9a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737269694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594329f431fd456d89c771444f5e662730713ccd58a9d03b52796bd7fa42e35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Aug 2021 23:23:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Aug 2021 23:23:52 GMT
ENV DOCKER_VERSION=20.10.8
# Tue, 24 Aug 2021 23:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.8.zip
# Tue, 24 Aug 2021 23:24:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4896faf56da9e635d1215c12a54c8734e695682b57d6e038ca62fd90b532b`  
		Last Modified: Tue, 24 Aug 2021 23:25:13 GMT  
		Size: 378.4 KB (378370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49ef5983ec79b546f9ba4e76c016df80499c33627052d1101b851ffb7b4fde`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8baf6cf9c02dbd2217455c62d5ee255fd65036a9a442d0d4794abb2fa68c59`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0b72a29873171e2e2cfc43d555ef003e482ffe643396157ba76e4b22ab3017`  
		Last Modified: Tue, 24 Aug 2021 23:26:06 GMT  
		Size: 50.9 MB (50889387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:cbf25f4f97f8ab21eabc463af9798d733fbb32b3a34483d5ba74b1bff914910c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:35f612c47195c6e7c1e9ecc80c1b1a00402f3c039e768dd08b2ddb237fd5d0ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66151138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67ee0b7de2f5cca0d60fe996f082ee6795d35fdd0c7823325b0f7855f57c342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2fad5f90265a7c9c4ee73f0b0eaa7b5ed8203af4cd0464dda8f7e1f4b28a5ad7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60042992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3734d5adc5ac9557175d6c0acb930e7ed6d75e1f2e52e8c170b4ade3f76806a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:b1b2943cc94fa1b87be7d612656f72f9a6f4132e96d7a5e4e4e35b383c6e3102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:d1c7515d7ba19c572b6f60ec904cf0a875b3bf60c427205845b5ab7b432b05ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72680575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc41137f712d794c3471c40b56f946667cfe729e112ebc6f1a824bcc775f679`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 00:26:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:26:55 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 00:26:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 00:26:57 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:57 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 00:26:57 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 00:26:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:58 GMT
CMD []
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5973cffe69ed6ec4ab2e2a3a191794cfba7339588cdbc4f3c6355e040c05fb`  
		Last Modified: Wed, 01 Sep 2021 00:28:13 GMT  
		Size: 6.5 MB (6524532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a47d00d0a33090100f0be8b5d564e20357fa60a275aba922aea6db6fb47531`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8a29d06b5993e5468f57fa6a9d0adff807919d6c664b785a96b1fb6a96d8`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 978.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6762b64189d2495a0856c3f7d465d7ad0f91a4e2db42b4093e70c7b55e571211`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f21866d81ae3b92303af07fe477794e4e4bf43836de0d41b4c212d4469d41a1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66466448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de95d7c2e2d4cc59123fcfef69442499876a675bb59ab504b9ad78c5881fe85a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:39:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 21:39:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:45 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 21:39:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 21:39:46 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:47 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 21:39:47 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 21:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:47 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff707a384f2d3eeae1ec32f9044142bb5c896541416c18d1bf45142da30ae`  
		Last Modified: Wed, 01 Sep 2021 21:41:30 GMT  
		Size: 6.4 MB (6418561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d94df880147a87f1fba1c3115c37eb4b50c95fc93694f4d5e1fc22f353fd3`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ada35578ff611689fc1c810d1603dd6b6c606175e97737d9f3073f4631235b0`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcd3a1f2fec5765d757040410b3f777d30970931dd552544b55ada1dc9ebe8`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:99a866bf721d434fdda04b68126b8a8611b2f84633ce37c28814cd33ead91de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:33a0761966c87569be2a9763c8c477dd3e8981982c8abc4324c090f9d2478231
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92930272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5357717b590217cbd992209ed6e2fb34e8ba65a74d3a5324c9b916395a15cb1b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 00:26:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:26:55 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 00:26:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 00:26:57 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:57 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 00:26:57 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 00:26:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:58 GMT
CMD []
# Wed, 01 Sep 2021 00:27:03 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 00:27:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 00:27:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:27:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 00:27:07 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 00:27:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 00:27:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5973cffe69ed6ec4ab2e2a3a191794cfba7339588cdbc4f3c6355e040c05fb`  
		Last Modified: Wed, 01 Sep 2021 00:28:13 GMT  
		Size: 6.5 MB (6524532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a47d00d0a33090100f0be8b5d564e20357fa60a275aba922aea6db6fb47531`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8a29d06b5993e5468f57fa6a9d0adff807919d6c664b785a96b1fb6a96d8`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 978.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6762b64189d2495a0856c3f7d465d7ad0f91a4e2db42b4093e70c7b55e571211`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dbc14ca68582d0028413d0826f71ced2423d092126de153c91bbf05e4c98fa`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.1 MB (1131899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2498ce93d923f17fb67004858df28e840d729cf6e6fbdfa82ed3c82679ebe4`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64015873fa22ddcd58c65fa437669d9153f1a1fd72fd3a43dbd6873f129461b9`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcf73021c4287b49de963988902f36818158f72e0ccd6e3b93af6bb3f4e7ef9`  
		Last Modified: Wed, 01 Sep 2021 00:28:39 GMT  
		Size: 19.1 MB (19116093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ea275b05bd4bf7a61d8bc934c3d72b3d30ae866ed920fdd7d0a5d06933c0d`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:01a3353757a17aa2125c2a6181c436134d7a0055df0ef3ba323826350e1d0ff1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88731007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcfee17c3e4c3e92f1ae3c5a77520971a3633eebf269f8a4a895634a5ad06c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:39:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 21:39:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:45 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 21:39:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 21:39:46 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:47 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 21:39:47 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 21:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:47 GMT
CMD []
# Wed, 01 Sep 2021 21:39:55 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 21:39:56 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 21:39:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 21:39:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 21:39:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 21:39:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff707a384f2d3eeae1ec32f9044142bb5c896541416c18d1bf45142da30ae`  
		Last Modified: Wed, 01 Sep 2021 21:41:30 GMT  
		Size: 6.4 MB (6418561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d94df880147a87f1fba1c3115c37eb4b50c95fc93694f4d5e1fc22f353fd3`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ada35578ff611689fc1c810d1603dd6b6c606175e97737d9f3073f4631235b0`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcd3a1f2fec5765d757040410b3f777d30970931dd552544b55ada1dc9ebe8`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0727607c4852e6356bf01e7ea1c0d090e6100e1045cd881eca01515749b53e6`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 1.2 MB (1168111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee229379e57fe13e75a06a3453c3afa2ec3959e936165ad25b24fa00a2bec57`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5c0508be8bb4e91bd2c3895baa8ee248bf3b1bb5bd9d605a8c5da8b4aeff1a`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dc3c7f21a4603739eb746480b3aa01086f70941d2b2141504e7c7e796a1bab`  
		Last Modified: Wed, 01 Sep 2021 21:41:57 GMT  
		Size: 21.1 MB (21094732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da3b6b5f43f82f2e3e8c853aefbe98b52cbd1ff0fc99294851db16ee9eefa2f`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:f830e24b3e166774970348fc36ea0e9d108e908e93f7ba6c6c206f2f12faf758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:709ceab8cd1164fbf0c03b1991f8f412a1543023548fa7a30de2268d399723aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d03657b093bb281e2bf0c19460dbf0f73fbf181780da767109363461960b6de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:27:13 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8c9f33643fb8321012f52f6a1ec572b42b9f29dcd29c0dcf2635ad0c9d1911`  
		Last Modified: Wed, 01 Sep 2021 00:29:00 GMT  
		Size: 6.4 MB (6402499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4951d55d07df56eb3dc8823e5abb438f05ced009af250666aab6381f9ef2a99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66784792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c1f1eae55906bc481ffd709ea71e35a3f9aa3dde59572a62cadf79d7442716`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:40:07 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac87a5e4495fa9d6f260ed353f2f2ed60461d2ccc2fcce309f3a0ab5cfe2a01`  
		Last Modified: Wed, 01 Sep 2021 21:42:18 GMT  
		Size: 6.7 MB (6741800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:81d849a5208118837827efb4f0433db49a305260c37f83ff813590c03521247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull docker@sha256:a86536c27f22717fed9d5bcb2ff43eb82f0c2e7eb602d6b9c5d714cd0b706e9a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737269694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594329f431fd456d89c771444f5e662730713ccd58a9d03b52796bd7fa42e35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Aug 2021 23:23:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Aug 2021 23:23:52 GMT
ENV DOCKER_VERSION=20.10.8
# Tue, 24 Aug 2021 23:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.8.zip
# Tue, 24 Aug 2021 23:24:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4896faf56da9e635d1215c12a54c8734e695682b57d6e038ca62fd90b532b`  
		Last Modified: Tue, 24 Aug 2021 23:25:13 GMT  
		Size: 378.4 KB (378370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49ef5983ec79b546f9ba4e76c016df80499c33627052d1101b851ffb7b4fde`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8baf6cf9c02dbd2217455c62d5ee255fd65036a9a442d0d4794abb2fa68c59`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0b72a29873171e2e2cfc43d555ef003e482ffe643396157ba76e4b22ab3017`  
		Last Modified: Tue, 24 Aug 2021 23:26:06 GMT  
		Size: 50.9 MB (50889387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:81d849a5208118837827efb4f0433db49a305260c37f83ff813590c03521247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull docker@sha256:a86536c27f22717fed9d5bcb2ff43eb82f0c2e7eb602d6b9c5d714cd0b706e9a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737269694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594329f431fd456d89c771444f5e662730713ccd58a9d03b52796bd7fa42e35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Aug 2021 23:23:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Aug 2021 23:23:52 GMT
ENV DOCKER_VERSION=20.10.8
# Tue, 24 Aug 2021 23:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.8.zip
# Tue, 24 Aug 2021 23:24:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4896faf56da9e635d1215c12a54c8734e695682b57d6e038ca62fd90b532b`  
		Last Modified: Tue, 24 Aug 2021 23:25:13 GMT  
		Size: 378.4 KB (378370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49ef5983ec79b546f9ba4e76c016df80499c33627052d1101b851ffb7b4fde`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8baf6cf9c02dbd2217455c62d5ee255fd65036a9a442d0d4794abb2fa68c59`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0b72a29873171e2e2cfc43d555ef003e482ffe643396157ba76e4b22ab3017`  
		Last Modified: Tue, 24 Aug 2021 23:26:06 GMT  
		Size: 50.9 MB (50889387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.8`

```console
$ docker pull docker@sha256:cbf25f4f97f8ab21eabc463af9798d733fbb32b3a34483d5ba74b1bff914910c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.8` - linux; amd64

```console
$ docker pull docker@sha256:35f612c47195c6e7c1e9ecc80c1b1a00402f3c039e768dd08b2ddb237fd5d0ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66151138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67ee0b7de2f5cca0d60fe996f082ee6795d35fdd0c7823325b0f7855f57c342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.8` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2fad5f90265a7c9c4ee73f0b0eaa7b5ed8203af4cd0464dda8f7e1f4b28a5ad7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60042992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3734d5adc5ac9557175d6c0acb930e7ed6d75e1f2e52e8c170b4ade3f76806a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.8-alpine3.14`

```console
$ docker pull docker@sha256:071eb1f5e5122495faf6fcb69fbcc919363b176c0a81d7ab6808488ae3820e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:20.10.8-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2fad5f90265a7c9c4ee73f0b0eaa7b5ed8203af4cd0464dda8f7e1f4b28a5ad7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60042992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3734d5adc5ac9557175d6c0acb930e7ed6d75e1f2e52e8c170b4ade3f76806a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.8-dind`

```console
$ docker pull docker@sha256:b1b2943cc94fa1b87be7d612656f72f9a6f4132e96d7a5e4e4e35b383c6e3102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.8-dind` - linux; amd64

```console
$ docker pull docker@sha256:d1c7515d7ba19c572b6f60ec904cf0a875b3bf60c427205845b5ab7b432b05ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72680575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc41137f712d794c3471c40b56f946667cfe729e112ebc6f1a824bcc775f679`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 00:26:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:26:55 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 00:26:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 00:26:57 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:57 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 00:26:57 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 00:26:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:58 GMT
CMD []
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5973cffe69ed6ec4ab2e2a3a191794cfba7339588cdbc4f3c6355e040c05fb`  
		Last Modified: Wed, 01 Sep 2021 00:28:13 GMT  
		Size: 6.5 MB (6524532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a47d00d0a33090100f0be8b5d564e20357fa60a275aba922aea6db6fb47531`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8a29d06b5993e5468f57fa6a9d0adff807919d6c664b785a96b1fb6a96d8`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 978.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6762b64189d2495a0856c3f7d465d7ad0f91a4e2db42b4093e70c7b55e571211`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.8-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f21866d81ae3b92303af07fe477794e4e4bf43836de0d41b4c212d4469d41a1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66466448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de95d7c2e2d4cc59123fcfef69442499876a675bb59ab504b9ad78c5881fe85a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:39:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 21:39:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:45 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 21:39:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 21:39:46 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:47 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 21:39:47 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 21:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:47 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff707a384f2d3eeae1ec32f9044142bb5c896541416c18d1bf45142da30ae`  
		Last Modified: Wed, 01 Sep 2021 21:41:30 GMT  
		Size: 6.4 MB (6418561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d94df880147a87f1fba1c3115c37eb4b50c95fc93694f4d5e1fc22f353fd3`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ada35578ff611689fc1c810d1603dd6b6c606175e97737d9f3073f4631235b0`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcd3a1f2fec5765d757040410b3f777d30970931dd552544b55ada1dc9ebe8`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.8-dind-alpine3.14`

```console
$ docker pull docker@sha256:d600b32a04c7bc15485e1c3d29240e0cc3c6002d478b54c0c7da5657909be04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:20.10.8-dind-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f21866d81ae3b92303af07fe477794e4e4bf43836de0d41b4c212d4469d41a1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66466448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de95d7c2e2d4cc59123fcfef69442499876a675bb59ab504b9ad78c5881fe85a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:39:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 21:39:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:45 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 21:39:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 21:39:46 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:47 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 21:39:47 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 21:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:47 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff707a384f2d3eeae1ec32f9044142bb5c896541416c18d1bf45142da30ae`  
		Last Modified: Wed, 01 Sep 2021 21:41:30 GMT  
		Size: 6.4 MB (6418561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d94df880147a87f1fba1c3115c37eb4b50c95fc93694f4d5e1fc22f353fd3`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ada35578ff611689fc1c810d1603dd6b6c606175e97737d9f3073f4631235b0`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcd3a1f2fec5765d757040410b3f777d30970931dd552544b55ada1dc9ebe8`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.8-dind-rootless`

```console
$ docker pull docker@sha256:99a866bf721d434fdda04b68126b8a8611b2f84633ce37c28814cd33ead91de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.8-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:33a0761966c87569be2a9763c8c477dd3e8981982c8abc4324c090f9d2478231
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92930272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5357717b590217cbd992209ed6e2fb34e8ba65a74d3a5324c9b916395a15cb1b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 00:26:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:26:55 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 00:26:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 00:26:57 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:57 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 00:26:57 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 00:26:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:58 GMT
CMD []
# Wed, 01 Sep 2021 00:27:03 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 00:27:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 00:27:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:27:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 00:27:07 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 00:27:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 00:27:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5973cffe69ed6ec4ab2e2a3a191794cfba7339588cdbc4f3c6355e040c05fb`  
		Last Modified: Wed, 01 Sep 2021 00:28:13 GMT  
		Size: 6.5 MB (6524532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a47d00d0a33090100f0be8b5d564e20357fa60a275aba922aea6db6fb47531`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8a29d06b5993e5468f57fa6a9d0adff807919d6c664b785a96b1fb6a96d8`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 978.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6762b64189d2495a0856c3f7d465d7ad0f91a4e2db42b4093e70c7b55e571211`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dbc14ca68582d0028413d0826f71ced2423d092126de153c91bbf05e4c98fa`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.1 MB (1131899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2498ce93d923f17fb67004858df28e840d729cf6e6fbdfa82ed3c82679ebe4`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64015873fa22ddcd58c65fa437669d9153f1a1fd72fd3a43dbd6873f129461b9`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcf73021c4287b49de963988902f36818158f72e0ccd6e3b93af6bb3f4e7ef9`  
		Last Modified: Wed, 01 Sep 2021 00:28:39 GMT  
		Size: 19.1 MB (19116093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ea275b05bd4bf7a61d8bc934c3d72b3d30ae866ed920fdd7d0a5d06933c0d`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.8-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:01a3353757a17aa2125c2a6181c436134d7a0055df0ef3ba323826350e1d0ff1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88731007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcfee17c3e4c3e92f1ae3c5a77520971a3633eebf269f8a4a895634a5ad06c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:39:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 21:39:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:45 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 21:39:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 21:39:46 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:47 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 21:39:47 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 21:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:47 GMT
CMD []
# Wed, 01 Sep 2021 21:39:55 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 21:39:56 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 21:39:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 21:39:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 21:39:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 21:39:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff707a384f2d3eeae1ec32f9044142bb5c896541416c18d1bf45142da30ae`  
		Last Modified: Wed, 01 Sep 2021 21:41:30 GMT  
		Size: 6.4 MB (6418561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d94df880147a87f1fba1c3115c37eb4b50c95fc93694f4d5e1fc22f353fd3`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ada35578ff611689fc1c810d1603dd6b6c606175e97737d9f3073f4631235b0`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcd3a1f2fec5765d757040410b3f777d30970931dd552544b55ada1dc9ebe8`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0727607c4852e6356bf01e7ea1c0d090e6100e1045cd881eca01515749b53e6`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 1.2 MB (1168111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee229379e57fe13e75a06a3453c3afa2ec3959e936165ad25b24fa00a2bec57`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5c0508be8bb4e91bd2c3895baa8ee248bf3b1bb5bd9d605a8c5da8b4aeff1a`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dc3c7f21a4603739eb746480b3aa01086f70941d2b2141504e7c7e796a1bab`  
		Last Modified: Wed, 01 Sep 2021 21:41:57 GMT  
		Size: 21.1 MB (21094732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da3b6b5f43f82f2e3e8c853aefbe98b52cbd1ff0fc99294851db16ee9eefa2f`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.8-git`

```console
$ docker pull docker@sha256:f830e24b3e166774970348fc36ea0e9d108e908e93f7ba6c6c206f2f12faf758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.8-git` - linux; amd64

```console
$ docker pull docker@sha256:709ceab8cd1164fbf0c03b1991f8f412a1543023548fa7a30de2268d399723aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d03657b093bb281e2bf0c19460dbf0f73fbf181780da767109363461960b6de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:27:13 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8c9f33643fb8321012f52f6a1ec572b42b9f29dcd29c0dcf2635ad0c9d1911`  
		Last Modified: Wed, 01 Sep 2021 00:29:00 GMT  
		Size: 6.4 MB (6402499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.8-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4951d55d07df56eb3dc8823e5abb438f05ced009af250666aab6381f9ef2a99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66784792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c1f1eae55906bc481ffd709ea71e35a3f9aa3dde59572a62cadf79d7442716`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:40:07 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac87a5e4495fa9d6f260ed353f2f2ed60461d2ccc2fcce309f3a0ab5cfe2a01`  
		Last Modified: Wed, 01 Sep 2021 21:42:18 GMT  
		Size: 6.7 MB (6741800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.8-windowsservercore`

```console
$ docker pull docker@sha256:81d849a5208118837827efb4f0433db49a305260c37f83ff813590c03521247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `docker:20.10.8-windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull docker@sha256:a86536c27f22717fed9d5bcb2ff43eb82f0c2e7eb602d6b9c5d714cd0b706e9a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737269694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594329f431fd456d89c771444f5e662730713ccd58a9d03b52796bd7fa42e35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Aug 2021 23:23:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Aug 2021 23:23:52 GMT
ENV DOCKER_VERSION=20.10.8
# Tue, 24 Aug 2021 23:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.8.zip
# Tue, 24 Aug 2021 23:24:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4896faf56da9e635d1215c12a54c8734e695682b57d6e038ca62fd90b532b`  
		Last Modified: Tue, 24 Aug 2021 23:25:13 GMT  
		Size: 378.4 KB (378370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49ef5983ec79b546f9ba4e76c016df80499c33627052d1101b851ffb7b4fde`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8baf6cf9c02dbd2217455c62d5ee255fd65036a9a442d0d4794abb2fa68c59`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0b72a29873171e2e2cfc43d555ef003e482ffe643396157ba76e4b22ab3017`  
		Last Modified: Tue, 24 Aug 2021 23:26:06 GMT  
		Size: 50.9 MB (50889387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.8-windowsservercore-1809`

```console
$ docker pull docker@sha256:81d849a5208118837827efb4f0433db49a305260c37f83ff813590c03521247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `docker:20.10.8-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull docker@sha256:a86536c27f22717fed9d5bcb2ff43eb82f0c2e7eb602d6b9c5d714cd0b706e9a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737269694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594329f431fd456d89c771444f5e662730713ccd58a9d03b52796bd7fa42e35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Aug 2021 23:23:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Aug 2021 23:23:52 GMT
ENV DOCKER_VERSION=20.10.8
# Tue, 24 Aug 2021 23:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.8.zip
# Tue, 24 Aug 2021 23:24:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4896faf56da9e635d1215c12a54c8734e695682b57d6e038ca62fd90b532b`  
		Last Modified: Tue, 24 Aug 2021 23:25:13 GMT  
		Size: 378.4 KB (378370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49ef5983ec79b546f9ba4e76c016df80499c33627052d1101b851ffb7b4fde`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8baf6cf9c02dbd2217455c62d5ee255fd65036a9a442d0d4794abb2fa68c59`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0b72a29873171e2e2cfc43d555ef003e482ffe643396157ba76e4b22ab3017`  
		Last Modified: Tue, 24 Aug 2021 23:26:06 GMT  
		Size: 50.9 MB (50889387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:b1b2943cc94fa1b87be7d612656f72f9a6f4132e96d7a5e4e4e35b383c6e3102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:d1c7515d7ba19c572b6f60ec904cf0a875b3bf60c427205845b5ab7b432b05ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72680575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc41137f712d794c3471c40b56f946667cfe729e112ebc6f1a824bcc775f679`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 00:26:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:26:55 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 00:26:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 00:26:57 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:57 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 00:26:57 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 00:26:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:58 GMT
CMD []
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5973cffe69ed6ec4ab2e2a3a191794cfba7339588cdbc4f3c6355e040c05fb`  
		Last Modified: Wed, 01 Sep 2021 00:28:13 GMT  
		Size: 6.5 MB (6524532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a47d00d0a33090100f0be8b5d564e20357fa60a275aba922aea6db6fb47531`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8a29d06b5993e5468f57fa6a9d0adff807919d6c664b785a96b1fb6a96d8`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 978.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6762b64189d2495a0856c3f7d465d7ad0f91a4e2db42b4093e70c7b55e571211`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f21866d81ae3b92303af07fe477794e4e4bf43836de0d41b4c212d4469d41a1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66466448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de95d7c2e2d4cc59123fcfef69442499876a675bb59ab504b9ad78c5881fe85a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:39:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 21:39:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:45 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 21:39:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 21:39:46 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:47 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 21:39:47 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 21:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:47 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff707a384f2d3eeae1ec32f9044142bb5c896541416c18d1bf45142da30ae`  
		Last Modified: Wed, 01 Sep 2021 21:41:30 GMT  
		Size: 6.4 MB (6418561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d94df880147a87f1fba1c3115c37eb4b50c95fc93694f4d5e1fc22f353fd3`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ada35578ff611689fc1c810d1603dd6b6c606175e97737d9f3073f4631235b0`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcd3a1f2fec5765d757040410b3f777d30970931dd552544b55ada1dc9ebe8`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:99a866bf721d434fdda04b68126b8a8611b2f84633ce37c28814cd33ead91de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:33a0761966c87569be2a9763c8c477dd3e8981982c8abc4324c090f9d2478231
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92930272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5357717b590217cbd992209ed6e2fb34e8ba65a74d3a5324c9b916395a15cb1b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 00:26:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:26:55 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 00:26:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 00:26:57 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:57 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 00:26:57 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 00:26:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:58 GMT
CMD []
# Wed, 01 Sep 2021 00:27:03 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 00:27:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 00:27:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:27:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 00:27:07 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 00:27:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 00:27:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5973cffe69ed6ec4ab2e2a3a191794cfba7339588cdbc4f3c6355e040c05fb`  
		Last Modified: Wed, 01 Sep 2021 00:28:13 GMT  
		Size: 6.5 MB (6524532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a47d00d0a33090100f0be8b5d564e20357fa60a275aba922aea6db6fb47531`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8a29d06b5993e5468f57fa6a9d0adff807919d6c664b785a96b1fb6a96d8`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 978.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6762b64189d2495a0856c3f7d465d7ad0f91a4e2db42b4093e70c7b55e571211`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dbc14ca68582d0028413d0826f71ced2423d092126de153c91bbf05e4c98fa`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.1 MB (1131899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2498ce93d923f17fb67004858df28e840d729cf6e6fbdfa82ed3c82679ebe4`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64015873fa22ddcd58c65fa437669d9153f1a1fd72fd3a43dbd6873f129461b9`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcf73021c4287b49de963988902f36818158f72e0ccd6e3b93af6bb3f4e7ef9`  
		Last Modified: Wed, 01 Sep 2021 00:28:39 GMT  
		Size: 19.1 MB (19116093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ea275b05bd4bf7a61d8bc934c3d72b3d30ae866ed920fdd7d0a5d06933c0d`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:01a3353757a17aa2125c2a6181c436134d7a0055df0ef3ba323826350e1d0ff1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88731007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcfee17c3e4c3e92f1ae3c5a77520971a3633eebf269f8a4a895634a5ad06c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:39:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 21:39:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:45 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 21:39:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 21:39:46 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:47 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 21:39:47 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 21:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:47 GMT
CMD []
# Wed, 01 Sep 2021 21:39:55 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 21:39:56 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 21:39:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 21:39:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 21:39:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 21:39:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 21:39:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff707a384f2d3eeae1ec32f9044142bb5c896541416c18d1bf45142da30ae`  
		Last Modified: Wed, 01 Sep 2021 21:41:30 GMT  
		Size: 6.4 MB (6418561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d94df880147a87f1fba1c3115c37eb4b50c95fc93694f4d5e1fc22f353fd3`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ada35578ff611689fc1c810d1603dd6b6c606175e97737d9f3073f4631235b0`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcd3a1f2fec5765d757040410b3f777d30970931dd552544b55ada1dc9ebe8`  
		Last Modified: Wed, 01 Sep 2021 21:41:29 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0727607c4852e6356bf01e7ea1c0d090e6100e1045cd881eca01515749b53e6`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 1.2 MB (1168111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee229379e57fe13e75a06a3453c3afa2ec3959e936165ad25b24fa00a2bec57`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5c0508be8bb4e91bd2c3895baa8ee248bf3b1bb5bd9d605a8c5da8b4aeff1a`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dc3c7f21a4603739eb746480b3aa01086f70941d2b2141504e7c7e796a1bab`  
		Last Modified: Wed, 01 Sep 2021 21:41:57 GMT  
		Size: 21.1 MB (21094732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da3b6b5f43f82f2e3e8c853aefbe98b52cbd1ff0fc99294851db16ee9eefa2f`  
		Last Modified: Wed, 01 Sep 2021 21:41:53 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:f830e24b3e166774970348fc36ea0e9d108e908e93f7ba6c6c206f2f12faf758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:709ceab8cd1164fbf0c03b1991f8f412a1543023548fa7a30de2268d399723aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d03657b093bb281e2bf0c19460dbf0f73fbf181780da767109363461960b6de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:27:13 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8c9f33643fb8321012f52f6a1ec572b42b9f29dcd29c0dcf2635ad0c9d1911`  
		Last Modified: Wed, 01 Sep 2021 00:29:00 GMT  
		Size: 6.4 MB (6402499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4951d55d07df56eb3dc8823e5abb438f05ced009af250666aab6381f9ef2a99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66784792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c1f1eae55906bc481ffd709ea71e35a3f9aa3dde59572a62cadf79d7442716`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 21:40:07 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac87a5e4495fa9d6f260ed353f2f2ed60461d2ccc2fcce309f3a0ab5cfe2a01`  
		Last Modified: Wed, 01 Sep 2021 21:42:18 GMT  
		Size: 6.7 MB (6741800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:cbf25f4f97f8ab21eabc463af9798d733fbb32b3a34483d5ba74b1bff914910c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:35f612c47195c6e7c1e9ecc80c1b1a00402f3c039e768dd08b2ddb237fd5d0ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66151138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67ee0b7de2f5cca0d60fe996f082ee6795d35fdd0c7823325b0f7855f57c342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2fad5f90265a7c9c4ee73f0b0eaa7b5ed8203af4cd0464dda8f7e1f4b28a5ad7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60042992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3734d5adc5ac9557175d6c0acb930e7ed6d75e1f2e52e8c170b4ade3f76806a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 21:39:28 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 21:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 21:39:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 21:39:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 21:39:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 21:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 21:39:34 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a48a30fd82efeed488ce352f8151d74bb4484cd178fc5fd08e6a8ccfc69560`  
		Last Modified: Wed, 01 Sep 2021 21:41:06 GMT  
		Size: 55.4 MB (55420270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb6b55a7508af4b07b8ca08ae9f62ea7c5aa6bf46bc94cca92c15f6f418faf`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8605ad73716feec4bef5573f92fe2b1472d4e43804d33bd45d3656b83af314c`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ddbc92192571b4db6ee00ea2473aa0cdb78b7628f95560f0571a4ac15e330a`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:81d849a5208118837827efb4f0433db49a305260c37f83ff813590c03521247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `docker:windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull docker@sha256:a86536c27f22717fed9d5bcb2ff43eb82f0c2e7eb602d6b9c5d714cd0b706e9a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737269694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594329f431fd456d89c771444f5e662730713ccd58a9d03b52796bd7fa42e35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Aug 2021 23:23:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Aug 2021 23:23:52 GMT
ENV DOCKER_VERSION=20.10.8
# Tue, 24 Aug 2021 23:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.8.zip
# Tue, 24 Aug 2021 23:24:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4896faf56da9e635d1215c12a54c8734e695682b57d6e038ca62fd90b532b`  
		Last Modified: Tue, 24 Aug 2021 23:25:13 GMT  
		Size: 378.4 KB (378370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49ef5983ec79b546f9ba4e76c016df80499c33627052d1101b851ffb7b4fde`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8baf6cf9c02dbd2217455c62d5ee255fd65036a9a442d0d4794abb2fa68c59`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0b72a29873171e2e2cfc43d555ef003e482ffe643396157ba76e4b22ab3017`  
		Last Modified: Tue, 24 Aug 2021 23:26:06 GMT  
		Size: 50.9 MB (50889387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:81d849a5208118837827efb4f0433db49a305260c37f83ff813590c03521247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull docker@sha256:a86536c27f22717fed9d5bcb2ff43eb82f0c2e7eb602d6b9c5d714cd0b706e9a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737269694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594329f431fd456d89c771444f5e662730713ccd58a9d03b52796bd7fa42e35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Aug 2021 23:23:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Aug 2021 23:23:52 GMT
ENV DOCKER_VERSION=20.10.8
# Tue, 24 Aug 2021 23:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.8.zip
# Tue, 24 Aug 2021 23:24:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4896faf56da9e635d1215c12a54c8734e695682b57d6e038ca62fd90b532b`  
		Last Modified: Tue, 24 Aug 2021 23:25:13 GMT  
		Size: 378.4 KB (378370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49ef5983ec79b546f9ba4e76c016df80499c33627052d1101b851ffb7b4fde`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8baf6cf9c02dbd2217455c62d5ee255fd65036a9a442d0d4794abb2fa68c59`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0b72a29873171e2e2cfc43d555ef003e482ffe643396157ba76e4b22ab3017`  
		Last Modified: Tue, 24 Aug 2021 23:26:06 GMT  
		Size: 50.9 MB (50889387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
