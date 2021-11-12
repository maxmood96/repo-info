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
-	[`docker:20.10.10`](#docker201010)
-	[`docker:20.10.10-alpine3.14`](#docker201010-alpine314)
-	[`docker:20.10.10-dind`](#docker201010-dind)
-	[`docker:20.10.10-dind-alpine3.14`](#docker201010-dind-alpine314)
-	[`docker:20.10.10-dind-rootless`](#docker201010-dind-rootless)
-	[`docker:20.10.10-git`](#docker201010-git)
-	[`docker:20.10.10-windowsservercore`](#docker201010-windowsservercore)
-	[`docker:20.10.10-windowsservercore-1809`](#docker201010-windowsservercore-1809)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)

## `docker:20`

```console
$ docker pull docker@sha256:9a54056645ef715b689e10dcb49fb7fea85944175419eeffcda587ea02562ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:bc99b4fea52b058d06c4f9cb45f9c8c27d10dc4d69f202e75f051ff60b5f4fe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68456418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b706a049f56e2f84f9b0ae680c7b0412b6766580f09576bab4dc7cff753c4dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86d706786c53c36cfb5e5f04b40461571f5b2197c2584b5454f1affa11fe1423
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62354097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4844bf2dfb03935afa7012263776fccca7f223bbb1fb71980971a9eb20804cd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:3242b020c92cece24e42740e5ae75306bde66b04eb1bcdf527a60f1416af8e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:04fd1a7a19db9f3d0a9d95ef5ad79db235875a8a73af6850e6c5c22bc84cf862
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74984029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646696d3b05ba82569ddaff6345806329dc6c177dd23e6827623b82b7ffd9e62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6158fe019d263ecf2bfc4cd4a6b226daeba46b999c54e0c5c09a2d002761ba2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b5255ca79508775b27f942872b667535135af33c213429656edc09b7113ba2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:39:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 21:39:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:39:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 21:39:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 21:39:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:51 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 21:39:52 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 21:39:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:54 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c83ad5e199b9616e70e2823333442de5659b21b99bd95fdbf0f26bd32a8d66`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 6.4 MB (6418426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c007eab1540e6cf80cf380e2ddc07dcac926a209e8e758634051991eca930e0`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa0c7f4d9d3e108af9b808ffc5a33a6bdad68d35f05218879d1db94e5f0bd`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a56b3142046bc8b06211ff96c01a64a2a6225c33dcdda8c249bcf0509fb19`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:6db2fcdac4a9b659cbc5ee9cbce64a825ad0d3030d22f8d467e15c404fed19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:edf71b73b3a20e77a4f8f69b37bc72582a114b278bd261d8648658d6c17cc857
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95259749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f3018944b3068b6ccad0cad95fe3712dcb72923cb2f4fcc11ac17e20c5f2b0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
# Fri, 12 Nov 2021 22:01:39 GMT
RUN apk add --no-cache iproute2
# Fri, 12 Nov 2021 22:01:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 12 Nov 2021 22:01:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 12 Nov 2021 22:01:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 12 Nov 2021 22:01:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 12 Nov 2021 22:01:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e65c32f7feb2ca545e5be325979514421ae6452ffbb39555fc0ff558185ee8`  
		Last Modified: Fri, 12 Nov 2021 22:03:35 GMT  
		Size: 1.1 MB (1149132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791493f35b317dccba1da11b14d192d4a6ad0990ca703af9d9d8ef4e2bb27648`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b52cb220a5b157d4e3fb7e5810ede9299e89837bdbaa456fe479a7ef63e38b8`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf41e4bfb164e2b3470d582411b00c27cbd6fef248d65721f8e831e13a6ef569`  
		Last Modified: Fri, 12 Nov 2021 22:03:38 GMT  
		Size: 19.1 MB (19124871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b220a5803c6b5f3c60d16c70f281c7fda036290f7734521becd337abc10338d3`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e26fd0517a4c0fbc4eb40b8d5f2443f01c564b1dfac2a3c8d7e2570003da586a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91048347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b27f2f5863c42063283c408be0496fe4464ee1bbe57523f31b6d407fdad209`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:39:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 21:39:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:39:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 21:39:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 21:39:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:51 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 21:39:52 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 21:39:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:54 GMT
CMD []
# Mon, 25 Oct 2021 21:40:02 GMT
RUN apk add --no-cache iproute2
# Mon, 25 Oct 2021 21:40:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 25 Oct 2021 21:40:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:40:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 25 Oct 2021 21:40:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 25 Oct 2021 21:40:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 25 Oct 2021 21:40:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c83ad5e199b9616e70e2823333442de5659b21b99bd95fdbf0f26bd32a8d66`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 6.4 MB (6418426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c007eab1540e6cf80cf380e2ddc07dcac926a209e8e758634051991eca930e0`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa0c7f4d9d3e108af9b808ffc5a33a6bdad68d35f05218879d1db94e5f0bd`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a56b3142046bc8b06211ff96c01a64a2a6225c33dcdda8c249bcf0509fb19`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c2bcb5ec7ed6127224db03c4a91d3b4e911f8073fdf7315c7cd05787d6fdd9`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 1.2 MB (1167848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c771a668c1bdcf3842853e5311737d9df14e0cabba221a2fb0558ccda7cb3`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b1ca4a8eb1f7c284d581857052131558b8a97cd9768239f381599982acbdc6`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cf60b94cc6138d54ac15a7bdba723717568c577ff05ffc7be4df9874f9c715`  
		Last Modified: Mon, 25 Oct 2021 21:41:52 GMT  
		Size: 21.1 MB (21101491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6dddf584595a25d2848920678270fce3a9db1f04a4ee8e14b8506b4e2683e9`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:7a3fa2171e331f361193a720c020ea17fd27996921a6a1f994a846d344e50b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:f268a917b445d72291c0fc9668f4b1b741f75841665ef7b61620eb97d66ace9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75087137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c7cb5cd3da7d62f8b618fa5ff42c6766ef3df03b7e0fd3f61495134bf8209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:02:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cc0be1abc487b32db89139b7ed719bedb57d01764e80fadf1efc3d736128e1`  
		Last Modified: Fri, 12 Nov 2021 22:03:57 GMT  
		Size: 6.6 MB (6630719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:32bbd13b99a67402783f9128edeb5e3fa6d77d04b58281b5089b793d716af015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69093153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8854ee26220837eff66b4cf79ae6751e3d96ffde324d81dc0e6c71bce2646`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:40:17 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6601404362298c677e6cc05fd14789ccc50f3eed083c4c1359fcea2b87651b0`  
		Last Modified: Mon, 25 Oct 2021 21:42:11 GMT  
		Size: 6.7 MB (6739056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:e78fd43bddf89f0b3f9d5266fb59b8ba2769522adb4326ccfde2a1b856e153d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `docker:20-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull docker@sha256:d2102d257c324e0947958ab0a8a8807f05e36018528ba3768f11f86af5aa7136
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2757355356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8e048835c8ded96f1d05b3f62d5a36e63f95be23c778988353454f8319e60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 19:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 19:07:03 GMT
ENV DOCKER_VERSION=20.10.10
# Wed, 10 Nov 2021 19:07:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Wed, 10 Nov 2021 19:08:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e42405e6d7d9caeb7c5a114493eca7f34351fae0fc2b77118957003b2f6c5f`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 356.8 KB (356764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efb00514c58c47a9419a2bac3d8988001d22da51c450ae8545f936e17194184`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b661cf25a033b7049ba6383f2e061f3df82b0e33395f3c5ca4dee2107a9c5d`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bad48a088de54a9ff738f053e6ac85f107a0e6d1ecdaac388ce1693297e44`  
		Last Modified: Wed, 10 Nov 2021 19:08:37 GMT  
		Size: 50.9 MB (50873430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:e78fd43bddf89f0b3f9d5266fb59b8ba2769522adb4326ccfde2a1b856e153d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull docker@sha256:d2102d257c324e0947958ab0a8a8807f05e36018528ba3768f11f86af5aa7136
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2757355356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8e048835c8ded96f1d05b3f62d5a36e63f95be23c778988353454f8319e60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 19:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 19:07:03 GMT
ENV DOCKER_VERSION=20.10.10
# Wed, 10 Nov 2021 19:07:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Wed, 10 Nov 2021 19:08:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e42405e6d7d9caeb7c5a114493eca7f34351fae0fc2b77118957003b2f6c5f`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 356.8 KB (356764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efb00514c58c47a9419a2bac3d8988001d22da51c450ae8545f936e17194184`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b661cf25a033b7049ba6383f2e061f3df82b0e33395f3c5ca4dee2107a9c5d`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bad48a088de54a9ff738f053e6ac85f107a0e6d1ecdaac388ce1693297e44`  
		Last Modified: Wed, 10 Nov 2021 19:08:37 GMT  
		Size: 50.9 MB (50873430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:9a54056645ef715b689e10dcb49fb7fea85944175419eeffcda587ea02562ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:bc99b4fea52b058d06c4f9cb45f9c8c27d10dc4d69f202e75f051ff60b5f4fe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68456418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b706a049f56e2f84f9b0ae680c7b0412b6766580f09576bab4dc7cff753c4dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86d706786c53c36cfb5e5f04b40461571f5b2197c2584b5454f1affa11fe1423
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62354097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4844bf2dfb03935afa7012263776fccca7f223bbb1fb71980971a9eb20804cd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:3242b020c92cece24e42740e5ae75306bde66b04eb1bcdf527a60f1416af8e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:04fd1a7a19db9f3d0a9d95ef5ad79db235875a8a73af6850e6c5c22bc84cf862
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74984029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646696d3b05ba82569ddaff6345806329dc6c177dd23e6827623b82b7ffd9e62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6158fe019d263ecf2bfc4cd4a6b226daeba46b999c54e0c5c09a2d002761ba2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b5255ca79508775b27f942872b667535135af33c213429656edc09b7113ba2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:39:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 21:39:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:39:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 21:39:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 21:39:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:51 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 21:39:52 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 21:39:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:54 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c83ad5e199b9616e70e2823333442de5659b21b99bd95fdbf0f26bd32a8d66`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 6.4 MB (6418426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c007eab1540e6cf80cf380e2ddc07dcac926a209e8e758634051991eca930e0`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa0c7f4d9d3e108af9b808ffc5a33a6bdad68d35f05218879d1db94e5f0bd`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a56b3142046bc8b06211ff96c01a64a2a6225c33dcdda8c249bcf0509fb19`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:6db2fcdac4a9b659cbc5ee9cbce64a825ad0d3030d22f8d467e15c404fed19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:edf71b73b3a20e77a4f8f69b37bc72582a114b278bd261d8648658d6c17cc857
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95259749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f3018944b3068b6ccad0cad95fe3712dcb72923cb2f4fcc11ac17e20c5f2b0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
# Fri, 12 Nov 2021 22:01:39 GMT
RUN apk add --no-cache iproute2
# Fri, 12 Nov 2021 22:01:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 12 Nov 2021 22:01:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 12 Nov 2021 22:01:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 12 Nov 2021 22:01:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 12 Nov 2021 22:01:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e65c32f7feb2ca545e5be325979514421ae6452ffbb39555fc0ff558185ee8`  
		Last Modified: Fri, 12 Nov 2021 22:03:35 GMT  
		Size: 1.1 MB (1149132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791493f35b317dccba1da11b14d192d4a6ad0990ca703af9d9d8ef4e2bb27648`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b52cb220a5b157d4e3fb7e5810ede9299e89837bdbaa456fe479a7ef63e38b8`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf41e4bfb164e2b3470d582411b00c27cbd6fef248d65721f8e831e13a6ef569`  
		Last Modified: Fri, 12 Nov 2021 22:03:38 GMT  
		Size: 19.1 MB (19124871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b220a5803c6b5f3c60d16c70f281c7fda036290f7734521becd337abc10338d3`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e26fd0517a4c0fbc4eb40b8d5f2443f01c564b1dfac2a3c8d7e2570003da586a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91048347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b27f2f5863c42063283c408be0496fe4464ee1bbe57523f31b6d407fdad209`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:39:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 21:39:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:39:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 21:39:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 21:39:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:51 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 21:39:52 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 21:39:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:54 GMT
CMD []
# Mon, 25 Oct 2021 21:40:02 GMT
RUN apk add --no-cache iproute2
# Mon, 25 Oct 2021 21:40:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 25 Oct 2021 21:40:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:40:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 25 Oct 2021 21:40:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 25 Oct 2021 21:40:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 25 Oct 2021 21:40:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c83ad5e199b9616e70e2823333442de5659b21b99bd95fdbf0f26bd32a8d66`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 6.4 MB (6418426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c007eab1540e6cf80cf380e2ddc07dcac926a209e8e758634051991eca930e0`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa0c7f4d9d3e108af9b808ffc5a33a6bdad68d35f05218879d1db94e5f0bd`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a56b3142046bc8b06211ff96c01a64a2a6225c33dcdda8c249bcf0509fb19`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c2bcb5ec7ed6127224db03c4a91d3b4e911f8073fdf7315c7cd05787d6fdd9`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 1.2 MB (1167848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c771a668c1bdcf3842853e5311737d9df14e0cabba221a2fb0558ccda7cb3`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b1ca4a8eb1f7c284d581857052131558b8a97cd9768239f381599982acbdc6`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cf60b94cc6138d54ac15a7bdba723717568c577ff05ffc7be4df9874f9c715`  
		Last Modified: Mon, 25 Oct 2021 21:41:52 GMT  
		Size: 21.1 MB (21101491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6dddf584595a25d2848920678270fce3a9db1f04a4ee8e14b8506b4e2683e9`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:7a3fa2171e331f361193a720c020ea17fd27996921a6a1f994a846d344e50b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:f268a917b445d72291c0fc9668f4b1b741f75841665ef7b61620eb97d66ace9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75087137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c7cb5cd3da7d62f8b618fa5ff42c6766ef3df03b7e0fd3f61495134bf8209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:02:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cc0be1abc487b32db89139b7ed719bedb57d01764e80fadf1efc3d736128e1`  
		Last Modified: Fri, 12 Nov 2021 22:03:57 GMT  
		Size: 6.6 MB (6630719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:32bbd13b99a67402783f9128edeb5e3fa6d77d04b58281b5089b793d716af015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69093153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8854ee26220837eff66b4cf79ae6751e3d96ffde324d81dc0e6c71bce2646`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:40:17 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6601404362298c677e6cc05fd14789ccc50f3eed083c4c1359fcea2b87651b0`  
		Last Modified: Mon, 25 Oct 2021 21:42:11 GMT  
		Size: 6.7 MB (6739056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:e78fd43bddf89f0b3f9d5266fb59b8ba2769522adb4326ccfde2a1b856e153d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull docker@sha256:d2102d257c324e0947958ab0a8a8807f05e36018528ba3768f11f86af5aa7136
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2757355356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8e048835c8ded96f1d05b3f62d5a36e63f95be23c778988353454f8319e60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 19:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 19:07:03 GMT
ENV DOCKER_VERSION=20.10.10
# Wed, 10 Nov 2021 19:07:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Wed, 10 Nov 2021 19:08:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e42405e6d7d9caeb7c5a114493eca7f34351fae0fc2b77118957003b2f6c5f`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 356.8 KB (356764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efb00514c58c47a9419a2bac3d8988001d22da51c450ae8545f936e17194184`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b661cf25a033b7049ba6383f2e061f3df82b0e33395f3c5ca4dee2107a9c5d`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bad48a088de54a9ff738f053e6ac85f107a0e6d1ecdaac388ce1693297e44`  
		Last Modified: Wed, 10 Nov 2021 19:08:37 GMT  
		Size: 50.9 MB (50873430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:e78fd43bddf89f0b3f9d5266fb59b8ba2769522adb4326ccfde2a1b856e153d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull docker@sha256:d2102d257c324e0947958ab0a8a8807f05e36018528ba3768f11f86af5aa7136
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2757355356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8e048835c8ded96f1d05b3f62d5a36e63f95be23c778988353454f8319e60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 19:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 19:07:03 GMT
ENV DOCKER_VERSION=20.10.10
# Wed, 10 Nov 2021 19:07:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Wed, 10 Nov 2021 19:08:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e42405e6d7d9caeb7c5a114493eca7f34351fae0fc2b77118957003b2f6c5f`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 356.8 KB (356764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efb00514c58c47a9419a2bac3d8988001d22da51c450ae8545f936e17194184`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b661cf25a033b7049ba6383f2e061f3df82b0e33395f3c5ca4dee2107a9c5d`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bad48a088de54a9ff738f053e6ac85f107a0e6d1ecdaac388ce1693297e44`  
		Last Modified: Wed, 10 Nov 2021 19:08:37 GMT  
		Size: 50.9 MB (50873430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10`

```console
$ docker pull docker@sha256:9a54056645ef715b689e10dcb49fb7fea85944175419eeffcda587ea02562ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10` - linux; amd64

```console
$ docker pull docker@sha256:bc99b4fea52b058d06c4f9cb45f9c8c27d10dc4d69f202e75f051ff60b5f4fe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68456418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b706a049f56e2f84f9b0ae680c7b0412b6766580f09576bab4dc7cff753c4dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86d706786c53c36cfb5e5f04b40461571f5b2197c2584b5454f1affa11fe1423
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62354097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4844bf2dfb03935afa7012263776fccca7f223bbb1fb71980971a9eb20804cd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-alpine3.14`

```console
$ docker pull docker@sha256:9a54056645ef715b689e10dcb49fb7fea85944175419eeffcda587ea02562ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:bc99b4fea52b058d06c4f9cb45f9c8c27d10dc4d69f202e75f051ff60b5f4fe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68456418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b706a049f56e2f84f9b0ae680c7b0412b6766580f09576bab4dc7cff753c4dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86d706786c53c36cfb5e5f04b40461571f5b2197c2584b5454f1affa11fe1423
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62354097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4844bf2dfb03935afa7012263776fccca7f223bbb1fb71980971a9eb20804cd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-dind`

```console
$ docker pull docker@sha256:3242b020c92cece24e42740e5ae75306bde66b04eb1bcdf527a60f1416af8e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:04fd1a7a19db9f3d0a9d95ef5ad79db235875a8a73af6850e6c5c22bc84cf862
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74984029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646696d3b05ba82569ddaff6345806329dc6c177dd23e6827623b82b7ffd9e62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6158fe019d263ecf2bfc4cd4a6b226daeba46b999c54e0c5c09a2d002761ba2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b5255ca79508775b27f942872b667535135af33c213429656edc09b7113ba2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:39:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 21:39:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:39:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 21:39:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 21:39:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:51 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 21:39:52 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 21:39:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:54 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c83ad5e199b9616e70e2823333442de5659b21b99bd95fdbf0f26bd32a8d66`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 6.4 MB (6418426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c007eab1540e6cf80cf380e2ddc07dcac926a209e8e758634051991eca930e0`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa0c7f4d9d3e108af9b808ffc5a33a6bdad68d35f05218879d1db94e5f0bd`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a56b3142046bc8b06211ff96c01a64a2a6225c33dcdda8c249bcf0509fb19`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-dind-alpine3.14`

```console
$ docker pull docker@sha256:3242b020c92cece24e42740e5ae75306bde66b04eb1bcdf527a60f1416af8e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-dind-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:04fd1a7a19db9f3d0a9d95ef5ad79db235875a8a73af6850e6c5c22bc84cf862
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74984029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646696d3b05ba82569ddaff6345806329dc6c177dd23e6827623b82b7ffd9e62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-dind-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6158fe019d263ecf2bfc4cd4a6b226daeba46b999c54e0c5c09a2d002761ba2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b5255ca79508775b27f942872b667535135af33c213429656edc09b7113ba2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:39:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 21:39:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:39:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 21:39:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 21:39:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:51 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 21:39:52 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 21:39:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:54 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c83ad5e199b9616e70e2823333442de5659b21b99bd95fdbf0f26bd32a8d66`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 6.4 MB (6418426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c007eab1540e6cf80cf380e2ddc07dcac926a209e8e758634051991eca930e0`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa0c7f4d9d3e108af9b808ffc5a33a6bdad68d35f05218879d1db94e5f0bd`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a56b3142046bc8b06211ff96c01a64a2a6225c33dcdda8c249bcf0509fb19`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-dind-rootless`

```console
$ docker pull docker@sha256:6db2fcdac4a9b659cbc5ee9cbce64a825ad0d3030d22f8d467e15c404fed19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:edf71b73b3a20e77a4f8f69b37bc72582a114b278bd261d8648658d6c17cc857
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95259749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f3018944b3068b6ccad0cad95fe3712dcb72923cb2f4fcc11ac17e20c5f2b0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
# Fri, 12 Nov 2021 22:01:39 GMT
RUN apk add --no-cache iproute2
# Fri, 12 Nov 2021 22:01:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 12 Nov 2021 22:01:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 12 Nov 2021 22:01:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 12 Nov 2021 22:01:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 12 Nov 2021 22:01:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e65c32f7feb2ca545e5be325979514421ae6452ffbb39555fc0ff558185ee8`  
		Last Modified: Fri, 12 Nov 2021 22:03:35 GMT  
		Size: 1.1 MB (1149132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791493f35b317dccba1da11b14d192d4a6ad0990ca703af9d9d8ef4e2bb27648`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b52cb220a5b157d4e3fb7e5810ede9299e89837bdbaa456fe479a7ef63e38b8`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf41e4bfb164e2b3470d582411b00c27cbd6fef248d65721f8e831e13a6ef569`  
		Last Modified: Fri, 12 Nov 2021 22:03:38 GMT  
		Size: 19.1 MB (19124871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b220a5803c6b5f3c60d16c70f281c7fda036290f7734521becd337abc10338d3`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e26fd0517a4c0fbc4eb40b8d5f2443f01c564b1dfac2a3c8d7e2570003da586a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91048347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b27f2f5863c42063283c408be0496fe4464ee1bbe57523f31b6d407fdad209`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:39:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 21:39:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:39:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 21:39:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 21:39:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:51 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 21:39:52 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 21:39:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:54 GMT
CMD []
# Mon, 25 Oct 2021 21:40:02 GMT
RUN apk add --no-cache iproute2
# Mon, 25 Oct 2021 21:40:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 25 Oct 2021 21:40:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:40:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 25 Oct 2021 21:40:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 25 Oct 2021 21:40:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 25 Oct 2021 21:40:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c83ad5e199b9616e70e2823333442de5659b21b99bd95fdbf0f26bd32a8d66`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 6.4 MB (6418426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c007eab1540e6cf80cf380e2ddc07dcac926a209e8e758634051991eca930e0`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa0c7f4d9d3e108af9b808ffc5a33a6bdad68d35f05218879d1db94e5f0bd`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a56b3142046bc8b06211ff96c01a64a2a6225c33dcdda8c249bcf0509fb19`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c2bcb5ec7ed6127224db03c4a91d3b4e911f8073fdf7315c7cd05787d6fdd9`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 1.2 MB (1167848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c771a668c1bdcf3842853e5311737d9df14e0cabba221a2fb0558ccda7cb3`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b1ca4a8eb1f7c284d581857052131558b8a97cd9768239f381599982acbdc6`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cf60b94cc6138d54ac15a7bdba723717568c577ff05ffc7be4df9874f9c715`  
		Last Modified: Mon, 25 Oct 2021 21:41:52 GMT  
		Size: 21.1 MB (21101491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6dddf584595a25d2848920678270fce3a9db1f04a4ee8e14b8506b4e2683e9`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-git`

```console
$ docker pull docker@sha256:7a3fa2171e331f361193a720c020ea17fd27996921a6a1f994a846d344e50b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-git` - linux; amd64

```console
$ docker pull docker@sha256:f268a917b445d72291c0fc9668f4b1b741f75841665ef7b61620eb97d66ace9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75087137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c7cb5cd3da7d62f8b618fa5ff42c6766ef3df03b7e0fd3f61495134bf8209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:02:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cc0be1abc487b32db89139b7ed719bedb57d01764e80fadf1efc3d736128e1`  
		Last Modified: Fri, 12 Nov 2021 22:03:57 GMT  
		Size: 6.6 MB (6630719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:32bbd13b99a67402783f9128edeb5e3fa6d77d04b58281b5089b793d716af015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69093153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8854ee26220837eff66b4cf79ae6751e3d96ffde324d81dc0e6c71bce2646`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:40:17 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6601404362298c677e6cc05fd14789ccc50f3eed083c4c1359fcea2b87651b0`  
		Last Modified: Mon, 25 Oct 2021 21:42:11 GMT  
		Size: 6.7 MB (6739056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-windowsservercore`

```console
$ docker pull docker@sha256:e78fd43bddf89f0b3f9d5266fb59b8ba2769522adb4326ccfde2a1b856e153d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `docker:20.10.10-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull docker@sha256:d2102d257c324e0947958ab0a8a8807f05e36018528ba3768f11f86af5aa7136
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2757355356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8e048835c8ded96f1d05b3f62d5a36e63f95be23c778988353454f8319e60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 19:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 19:07:03 GMT
ENV DOCKER_VERSION=20.10.10
# Wed, 10 Nov 2021 19:07:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Wed, 10 Nov 2021 19:08:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e42405e6d7d9caeb7c5a114493eca7f34351fae0fc2b77118957003b2f6c5f`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 356.8 KB (356764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efb00514c58c47a9419a2bac3d8988001d22da51c450ae8545f936e17194184`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b661cf25a033b7049ba6383f2e061f3df82b0e33395f3c5ca4dee2107a9c5d`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bad48a088de54a9ff738f053e6ac85f107a0e6d1ecdaac388ce1693297e44`  
		Last Modified: Wed, 10 Nov 2021 19:08:37 GMT  
		Size: 50.9 MB (50873430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:e78fd43bddf89f0b3f9d5266fb59b8ba2769522adb4326ccfde2a1b856e153d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `docker:20.10.10-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull docker@sha256:d2102d257c324e0947958ab0a8a8807f05e36018528ba3768f11f86af5aa7136
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2757355356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8e048835c8ded96f1d05b3f62d5a36e63f95be23c778988353454f8319e60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 19:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 19:07:03 GMT
ENV DOCKER_VERSION=20.10.10
# Wed, 10 Nov 2021 19:07:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Wed, 10 Nov 2021 19:08:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e42405e6d7d9caeb7c5a114493eca7f34351fae0fc2b77118957003b2f6c5f`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 356.8 KB (356764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efb00514c58c47a9419a2bac3d8988001d22da51c450ae8545f936e17194184`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b661cf25a033b7049ba6383f2e061f3df82b0e33395f3c5ca4dee2107a9c5d`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bad48a088de54a9ff738f053e6ac85f107a0e6d1ecdaac388ce1693297e44`  
		Last Modified: Wed, 10 Nov 2021 19:08:37 GMT  
		Size: 50.9 MB (50873430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:3242b020c92cece24e42740e5ae75306bde66b04eb1bcdf527a60f1416af8e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:04fd1a7a19db9f3d0a9d95ef5ad79db235875a8a73af6850e6c5c22bc84cf862
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74984029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646696d3b05ba82569ddaff6345806329dc6c177dd23e6827623b82b7ffd9e62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6158fe019d263ecf2bfc4cd4a6b226daeba46b999c54e0c5c09a2d002761ba2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b5255ca79508775b27f942872b667535135af33c213429656edc09b7113ba2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:39:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 21:39:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:39:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 21:39:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 21:39:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:51 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 21:39:52 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 21:39:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:54 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c83ad5e199b9616e70e2823333442de5659b21b99bd95fdbf0f26bd32a8d66`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 6.4 MB (6418426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c007eab1540e6cf80cf380e2ddc07dcac926a209e8e758634051991eca930e0`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa0c7f4d9d3e108af9b808ffc5a33a6bdad68d35f05218879d1db94e5f0bd`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a56b3142046bc8b06211ff96c01a64a2a6225c33dcdda8c249bcf0509fb19`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:6db2fcdac4a9b659cbc5ee9cbce64a825ad0d3030d22f8d467e15c404fed19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:edf71b73b3a20e77a4f8f69b37bc72582a114b278bd261d8648658d6c17cc857
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95259749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f3018944b3068b6ccad0cad95fe3712dcb72923cb2f4fcc11ac17e20c5f2b0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
# Fri, 12 Nov 2021 22:01:39 GMT
RUN apk add --no-cache iproute2
# Fri, 12 Nov 2021 22:01:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 12 Nov 2021 22:01:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 12 Nov 2021 22:01:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 12 Nov 2021 22:01:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 12 Nov 2021 22:01:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e65c32f7feb2ca545e5be325979514421ae6452ffbb39555fc0ff558185ee8`  
		Last Modified: Fri, 12 Nov 2021 22:03:35 GMT  
		Size: 1.1 MB (1149132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791493f35b317dccba1da11b14d192d4a6ad0990ca703af9d9d8ef4e2bb27648`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b52cb220a5b157d4e3fb7e5810ede9299e89837bdbaa456fe479a7ef63e38b8`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf41e4bfb164e2b3470d582411b00c27cbd6fef248d65721f8e831e13a6ef569`  
		Last Modified: Fri, 12 Nov 2021 22:03:38 GMT  
		Size: 19.1 MB (19124871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b220a5803c6b5f3c60d16c70f281c7fda036290f7734521becd337abc10338d3`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e26fd0517a4c0fbc4eb40b8d5f2443f01c564b1dfac2a3c8d7e2570003da586a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91048347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b27f2f5863c42063283c408be0496fe4464ee1bbe57523f31b6d407fdad209`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:39:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 21:39:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:39:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 21:39:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 21:39:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:51 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 21:39:52 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 21:39:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:54 GMT
CMD []
# Mon, 25 Oct 2021 21:40:02 GMT
RUN apk add --no-cache iproute2
# Mon, 25 Oct 2021 21:40:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 25 Oct 2021 21:40:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 25 Oct 2021 21:40:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 25 Oct 2021 21:40:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 25 Oct 2021 21:40:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 25 Oct 2021 21:40:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c83ad5e199b9616e70e2823333442de5659b21b99bd95fdbf0f26bd32a8d66`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 6.4 MB (6418426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c007eab1540e6cf80cf380e2ddc07dcac926a209e8e758634051991eca930e0`  
		Last Modified: Mon, 25 Oct 2021 21:41:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa0c7f4d9d3e108af9b808ffc5a33a6bdad68d35f05218879d1db94e5f0bd`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a56b3142046bc8b06211ff96c01a64a2a6225c33dcdda8c249bcf0509fb19`  
		Last Modified: Mon, 25 Oct 2021 21:41:26 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c2bcb5ec7ed6127224db03c4a91d3b4e911f8073fdf7315c7cd05787d6fdd9`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 1.2 MB (1167848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c771a668c1bdcf3842853e5311737d9df14e0cabba221a2fb0558ccda7cb3`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b1ca4a8eb1f7c284d581857052131558b8a97cd9768239f381599982acbdc6`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cf60b94cc6138d54ac15a7bdba723717568c577ff05ffc7be4df9874f9c715`  
		Last Modified: Mon, 25 Oct 2021 21:41:52 GMT  
		Size: 21.1 MB (21101491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6dddf584595a25d2848920678270fce3a9db1f04a4ee8e14b8506b4e2683e9`  
		Last Modified: Mon, 25 Oct 2021 21:41:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:7a3fa2171e331f361193a720c020ea17fd27996921a6a1f994a846d344e50b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:f268a917b445d72291c0fc9668f4b1b741f75841665ef7b61620eb97d66ace9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75087137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c7cb5cd3da7d62f8b618fa5ff42c6766ef3df03b7e0fd3f61495134bf8209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:02:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cc0be1abc487b32db89139b7ed719bedb57d01764e80fadf1efc3d736128e1`  
		Last Modified: Fri, 12 Nov 2021 22:03:57 GMT  
		Size: 6.6 MB (6630719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:32bbd13b99a67402783f9128edeb5e3fa6d77d04b58281b5089b793d716af015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69093153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8854ee26220837eff66b4cf79ae6751e3d96ffde324d81dc0e6c71bce2646`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 21:40:17 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6601404362298c677e6cc05fd14789ccc50f3eed083c4c1359fcea2b87651b0`  
		Last Modified: Mon, 25 Oct 2021 21:42:11 GMT  
		Size: 6.7 MB (6739056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:9a54056645ef715b689e10dcb49fb7fea85944175419eeffcda587ea02562ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:bc99b4fea52b058d06c4f9cb45f9c8c27d10dc4d69f202e75f051ff60b5f4fe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68456418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b706a049f56e2f84f9b0ae680c7b0412b6766580f09576bab4dc7cff753c4dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86d706786c53c36cfb5e5f04b40461571f5b2197c2584b5454f1affa11fe1423
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62354097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4844bf2dfb03935afa7012263776fccca7f223bbb1fb71980971a9eb20804cd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Mon, 18 Oct 2021 21:39:51 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Oct 2021 21:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Oct 2021 21:39:25 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 21:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 21:39:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 21:39:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 21:39:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 21:39:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 21:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 21:39:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b9844ac93b529c1f52e7d493f8e6fe6192353fb1fb922d21c6170008e114d7`  
		Last Modified: Mon, 18 Oct 2021 21:42:47 GMT  
		Size: 1.9 MB (1909462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44145fb8198137b43c7a8143d29d785c2d628a41f9dd2d2c39a779bf8d89b128`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a0a2210ee49588730267d1d1b28f645d18df509f2e1edf23f79fe41e12051`  
		Last Modified: Mon, 25 Oct 2021 21:41:07 GMT  
		Size: 57.7 MB (57730976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eaed5488a6df6e8d01407c66db8a313c0f5435ba77124dbe266d11e811058c`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15793e77cc908f9e54f31ac8b333dec09e649498c1abd5f41511c84d31e622ab`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8e498474746e85596cece599e5654f17c1cd4966783361362f812c39e2ed6a`  
		Last Modified: Mon, 25 Oct 2021 21:40:57 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e78fd43bddf89f0b3f9d5266fb59b8ba2769522adb4326ccfde2a1b856e153d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `docker:windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull docker@sha256:d2102d257c324e0947958ab0a8a8807f05e36018528ba3768f11f86af5aa7136
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2757355356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8e048835c8ded96f1d05b3f62d5a36e63f95be23c778988353454f8319e60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 19:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 19:07:03 GMT
ENV DOCKER_VERSION=20.10.10
# Wed, 10 Nov 2021 19:07:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Wed, 10 Nov 2021 19:08:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e42405e6d7d9caeb7c5a114493eca7f34351fae0fc2b77118957003b2f6c5f`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 356.8 KB (356764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efb00514c58c47a9419a2bac3d8988001d22da51c450ae8545f936e17194184`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b661cf25a033b7049ba6383f2e061f3df82b0e33395f3c5ca4dee2107a9c5d`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bad48a088de54a9ff738f053e6ac85f107a0e6d1ecdaac388ce1693297e44`  
		Last Modified: Wed, 10 Nov 2021 19:08:37 GMT  
		Size: 50.9 MB (50873430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:e78fd43bddf89f0b3f9d5266fb59b8ba2769522adb4326ccfde2a1b856e153d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull docker@sha256:d2102d257c324e0947958ab0a8a8807f05e36018528ba3768f11f86af5aa7136
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2757355356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8e048835c8ded96f1d05b3f62d5a36e63f95be23c778988353454f8319e60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 19:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 19:07:03 GMT
ENV DOCKER_VERSION=20.10.10
# Wed, 10 Nov 2021 19:07:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.10.zip
# Wed, 10 Nov 2021 19:08:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e42405e6d7d9caeb7c5a114493eca7f34351fae0fc2b77118957003b2f6c5f`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 356.8 KB (356764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efb00514c58c47a9419a2bac3d8988001d22da51c450ae8545f936e17194184`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b661cf25a033b7049ba6383f2e061f3df82b0e33395f3c5ca4dee2107a9c5d`  
		Last Modified: Wed, 10 Nov 2021 19:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bad48a088de54a9ff738f053e6ac85f107a0e6d1ecdaac388ce1693297e44`  
		Last Modified: Wed, 10 Nov 2021 19:08:37 GMT  
		Size: 50.9 MB (50873430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
