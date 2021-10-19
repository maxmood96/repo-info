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
-	[`docker:20.10-rc`](#docker2010-rc)
-	[`docker:20.10-rc-dind`](#docker2010-rc-dind)
-	[`docker:20.10-rc-dind-rootless`](#docker2010-rc-dind-rootless)
-	[`docker:20.10-rc-git`](#docker2010-rc-git)
-	[`docker:20.10-rc-windowsservercore`](#docker2010-rc-windowsservercore)
-	[`docker:20.10-rc-windowsservercore-1809`](#docker2010-rc-windowsservercore-1809)
-	[`docker:20.10-windowsservercore`](#docker2010-windowsservercore)
-	[`docker:20.10-windowsservercore-1809`](#docker2010-windowsservercore-1809)
-	[`docker:20.10.10-rc1`](#docker201010-rc1)
-	[`docker:20.10.10-rc1-alpine3.14`](#docker201010-rc1-alpine314)
-	[`docker:20.10.10-rc1-dind`](#docker201010-rc1-dind)
-	[`docker:20.10.10-rc1-dind-alpine3.14`](#docker201010-rc1-dind-alpine314)
-	[`docker:20.10.10-rc1-dind-rootless`](#docker201010-rc1-dind-rootless)
-	[`docker:20.10.10-rc1-git`](#docker201010-rc1-git)
-	[`docker:20.10.10-rc1-windowsservercore`](#docker201010-rc1-windowsservercore)
-	[`docker:20.10.10-rc1-windowsservercore-1809`](#docker201010-rc1-windowsservercore-1809)
-	[`docker:20.10.9`](#docker20109)
-	[`docker:20.10.9-alpine3.14`](#docker20109-alpine314)
-	[`docker:20.10.9-dind`](#docker20109-dind)
-	[`docker:20.10.9-dind-alpine3.14`](#docker20109-dind-alpine314)
-	[`docker:20.10.9-dind-rootless`](#docker20109-dind-rootless)
-	[`docker:20.10.9-git`](#docker20109-git)
-	[`docker:20.10.9-windowsservercore`](#docker20109-windowsservercore)
-	[`docker:20.10.9-windowsservercore-1809`](#docker20109-windowsservercore-1809)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:rc`](#dockerrc)
-	[`docker:rc-dind`](#dockerrc-dind)
-	[`docker:rc-dind-rootless`](#dockerrc-dind-rootless)
-	[`docker:rc-git`](#dockerrc-git)
-	[`docker:rc-windowsservercore`](#dockerrc-windowsservercore)
-	[`docker:rc-windowsservercore-1809`](#dockerrc-windowsservercore-1809)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)

## `docker:20`

```console
$ docker pull docker@sha256:938bcb85cf77db2b80d219abd5a1424ec15ce11a3adaea6423fa16cc9acfe926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1710b19ecaa7eba8537ea64a35ddec333ff128cda5f2f19b7c4cd6e3a4e0daf7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c324afd4ac0437589f8f6e825c2fed8ef663773f55ac7c8e85cd589f554239d`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:d842418d21545fde57c2512681d9bdc4ce0e54f2e0305a293ee20a9b6166932b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3ba0867a449ca78b731e3251ddeb677fa893dc500293ab0e303a8188b9e4d106
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6144797d483747bee375b8607893579ff8b6d6ff47e83b10ed4827e4123f549e`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:09 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:41:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:41:12 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:41:12 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:41:13 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:41:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:41:15 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8bdd67624c83a9918b7d0bb7d24f84d32a306b3453ac55e213380ee17335d`  
		Last Modified: Mon, 18 Oct 2021 21:44:31 GMT  
		Size: 6.4 MB (6418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e9de043d240e7a3e0baf2f1a9bd6bd1da52fd1a1df9db1d97b50b294c98b8`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b746a27963c477864e414004aab19efff02e763e88444128d5bbf735410a4f`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f756b76c3b8328ed61cc3fef72a62229860b3a7fefcc6e94edda353b7d3a`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:51cd937b2ad1a1d32179f2e9acc01ea46d4e127cdaf493a533172b1fb019af15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:75acfc77a83d9b4d557aab529432058b78ac6d629325c9d61c385cd2fc48fe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95235937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4aec2427ffe9836431bca031ae4354053a010dae4736917b174d52da90dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
# Tue, 05 Oct 2021 17:32:44 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Oct 2021 17:32:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Oct 2021 17:32:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Oct 2021 17:32:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Oct 2021 17:32:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Oct 2021 17:32:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f850bf44d36d532f71a72ed317e54531b904953d99821dd316e73e777d23c`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.1 MB (1148745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03facf1a1e41afef60e2e7bad46f0fbd44f5b2b3a3328337c3e0a6049120dd8`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919e685bb3723d38cd895248bb1c99de9588af3aba7f57ef5cb72eca54106a9`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79573e4e685e01787d1e021ea1cecb99cdbf78577b160037c6ed2c7f8f2b304`  
		Last Modified: Tue, 05 Oct 2021 17:34:11 GMT  
		Size: 19.1 MB (19118054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7054ab8c007ff95ebed9750aae6c97b9f692ed317ea464234611c57db8601634`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:eb9feb96a9c979384276b169446b5134c441625461108344fde1f18fdee9ce75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91045261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a26cf3ffc31a4748452e2da3ca2a290c3354e441650e7617aaf4a9fbf6d1750`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:09 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:41:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:41:12 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:41:12 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:41:13 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:41:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:41:15 GMT
CMD []
# Mon, 18 Oct 2021 21:41:23 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 21:41:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 21:41:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 21:41:29 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 21:41:30 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 21:41:31 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8bdd67624c83a9918b7d0bb7d24f84d32a306b3453ac55e213380ee17335d`  
		Last Modified: Mon, 18 Oct 2021 21:44:31 GMT  
		Size: 6.4 MB (6418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e9de043d240e7a3e0baf2f1a9bd6bd1da52fd1a1df9db1d97b50b294c98b8`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b746a27963c477864e414004aab19efff02e763e88444128d5bbf735410a4f`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f756b76c3b8328ed61cc3fef72a62229860b3a7fefcc6e94edda353b7d3a`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da73c72dcad0b534b2f4febbace9688a2f4a30bf46b188501e200b3be5977b03`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 1.2 MB (1167836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ff4316d7dcf66341a4e5a7a7519ed9d36f902bb95d2169ebc26549a0f95849`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba611fb139d8c880c857badbc205cee357e35952ae811c52e90139e68f959d57`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098b6fcc42aecdd56305fc4ceba9415e977d589f359ff58a7ee2c72612859ce9`  
		Last Modified: Mon, 18 Oct 2021 21:44:55 GMT  
		Size: 21.1 MB (21096004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeef11aee822059479265f63f55446205a437ef50e49fbfb586c607571b58574`  
		Last Modified: Mon, 18 Oct 2021 21:44:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:370cbd65cbf44658bc2ce46c8b606213d9e3e3ea04a7d53a0243d67ca6db95aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:3bf13c54edb2a2b817bcad4ae459bf6d8b867930b5026d1f51d4593f598495fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75071530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed61dfae734a45e9440fbd932eeb2b244f0079a45398e33dd1478f62a4f3be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:54 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e22895e9057604af4145b328a599ef34ed98eee9085de276ad33fe1adf50f5f`  
		Last Modified: Tue, 05 Oct 2021 17:34:29 GMT  
		Size: 6.6 MB (6630406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6f7fe91a5a952fb482822be280a9c17313785627cdf33330c1980bf4404d6787
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69095577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1ae00454f4fd0beeab581baa00fe5961ae9b97bae5802e58bc1d0e49636a41`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:38 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae700626b8f4a7301ee4ec15808eb5b1b281fa56ecf42eb4a653b7f0b2a5f722`  
		Last Modified: Mon, 18 Oct 2021 21:45:15 GMT  
		Size: 6.7 MB (6739077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:938bcb85cf77db2b80d219abd5a1424ec15ce11a3adaea6423fa16cc9acfe926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1710b19ecaa7eba8537ea64a35ddec333ff128cda5f2f19b7c4cd6e3a4e0daf7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c324afd4ac0437589f8f6e825c2fed8ef663773f55ac7c8e85cd589f554239d`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:d842418d21545fde57c2512681d9bdc4ce0e54f2e0305a293ee20a9b6166932b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3ba0867a449ca78b731e3251ddeb677fa893dc500293ab0e303a8188b9e4d106
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6144797d483747bee375b8607893579ff8b6d6ff47e83b10ed4827e4123f549e`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:09 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:41:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:41:12 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:41:12 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:41:13 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:41:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:41:15 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8bdd67624c83a9918b7d0bb7d24f84d32a306b3453ac55e213380ee17335d`  
		Last Modified: Mon, 18 Oct 2021 21:44:31 GMT  
		Size: 6.4 MB (6418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e9de043d240e7a3e0baf2f1a9bd6bd1da52fd1a1df9db1d97b50b294c98b8`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b746a27963c477864e414004aab19efff02e763e88444128d5bbf735410a4f`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f756b76c3b8328ed61cc3fef72a62229860b3a7fefcc6e94edda353b7d3a`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:51cd937b2ad1a1d32179f2e9acc01ea46d4e127cdaf493a533172b1fb019af15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:75acfc77a83d9b4d557aab529432058b78ac6d629325c9d61c385cd2fc48fe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95235937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4aec2427ffe9836431bca031ae4354053a010dae4736917b174d52da90dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
# Tue, 05 Oct 2021 17:32:44 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Oct 2021 17:32:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Oct 2021 17:32:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Oct 2021 17:32:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Oct 2021 17:32:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Oct 2021 17:32:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f850bf44d36d532f71a72ed317e54531b904953d99821dd316e73e777d23c`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.1 MB (1148745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03facf1a1e41afef60e2e7bad46f0fbd44f5b2b3a3328337c3e0a6049120dd8`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919e685bb3723d38cd895248bb1c99de9588af3aba7f57ef5cb72eca54106a9`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79573e4e685e01787d1e021ea1cecb99cdbf78577b160037c6ed2c7f8f2b304`  
		Last Modified: Tue, 05 Oct 2021 17:34:11 GMT  
		Size: 19.1 MB (19118054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7054ab8c007ff95ebed9750aae6c97b9f692ed317ea464234611c57db8601634`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:eb9feb96a9c979384276b169446b5134c441625461108344fde1f18fdee9ce75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91045261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a26cf3ffc31a4748452e2da3ca2a290c3354e441650e7617aaf4a9fbf6d1750`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:09 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:41:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:41:12 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:41:12 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:41:13 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:41:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:41:15 GMT
CMD []
# Mon, 18 Oct 2021 21:41:23 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 21:41:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 21:41:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 21:41:29 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 21:41:30 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 21:41:31 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8bdd67624c83a9918b7d0bb7d24f84d32a306b3453ac55e213380ee17335d`  
		Last Modified: Mon, 18 Oct 2021 21:44:31 GMT  
		Size: 6.4 MB (6418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e9de043d240e7a3e0baf2f1a9bd6bd1da52fd1a1df9db1d97b50b294c98b8`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b746a27963c477864e414004aab19efff02e763e88444128d5bbf735410a4f`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f756b76c3b8328ed61cc3fef72a62229860b3a7fefcc6e94edda353b7d3a`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da73c72dcad0b534b2f4febbace9688a2f4a30bf46b188501e200b3be5977b03`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 1.2 MB (1167836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ff4316d7dcf66341a4e5a7a7519ed9d36f902bb95d2169ebc26549a0f95849`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba611fb139d8c880c857badbc205cee357e35952ae811c52e90139e68f959d57`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098b6fcc42aecdd56305fc4ceba9415e977d589f359ff58a7ee2c72612859ce9`  
		Last Modified: Mon, 18 Oct 2021 21:44:55 GMT  
		Size: 21.1 MB (21096004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeef11aee822059479265f63f55446205a437ef50e49fbfb586c607571b58574`  
		Last Modified: Mon, 18 Oct 2021 21:44:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:370cbd65cbf44658bc2ce46c8b606213d9e3e3ea04a7d53a0243d67ca6db95aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:3bf13c54edb2a2b817bcad4ae459bf6d8b867930b5026d1f51d4593f598495fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75071530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed61dfae734a45e9440fbd932eeb2b244f0079a45398e33dd1478f62a4f3be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:54 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e22895e9057604af4145b328a599ef34ed98eee9085de276ad33fe1adf50f5f`  
		Last Modified: Tue, 05 Oct 2021 17:34:29 GMT  
		Size: 6.6 MB (6630406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6f7fe91a5a952fb482822be280a9c17313785627cdf33330c1980bf4404d6787
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69095577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1ae00454f4fd0beeab581baa00fe5961ae9b97bae5802e58bc1d0e49636a41`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:38 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae700626b8f4a7301ee4ec15808eb5b1b281fa56ecf42eb4a653b7f0b2a5f722`  
		Last Modified: Mon, 18 Oct 2021 21:45:15 GMT  
		Size: 6.7 MB (6739077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc`

```console
$ docker pull docker@sha256:e52651216e0b5ac26e6af91dbf569f071278cead01facbe40f96a2c3f3d4c53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-rc` - linux; amd64

```console
$ docker pull docker@sha256:c1ae01d9bd863fb2c3c35c34372cae93bfb72f08b8c9b47ea04a1e3a2f1238a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68443074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d11a884b0af0757a193f413afd914f494ce5bfbbaf998f2e328877680d1a513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:eab2a4f03c6f78fa775f16495d33d5bd9db312068b14db9caa3b631968f19f57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62354582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd1e6d54b025850351cefe3112edff43a74d0a46d04ad08066c1ba8d7e2ea9d`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc-dind`

```console
$ docker pull docker@sha256:4891561b3f9b41e4cf68eae73192efb192a92501e1882c7b7b03c40a58efd53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:2f95928d1f82d2ffb79ef4877800c8490e3c86fecd4b2186e20807f6fd5480f6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74969409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36162799b0039f9f46374d98c63fcb428e69a89cf3f2dd0c766cc6df5d87b32c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 22:19:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:35 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 22:19:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 22:19:36 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:37 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 22:19:37 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 22:19:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425931fed24edf6259d6a6ddd00725a7195a42dd7bc0b70b0cc18d0d1aaa4396`  
		Last Modified: Mon, 18 Oct 2021 22:21:04 GMT  
		Size: 6.5 MB (6521438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a87d63582576ec7a470e771f6c5d16ff7cb7338024ea93995f04bfb4fe1199f`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9e7e65b6f97a6d64f396fdfbbfdf24802e58a822b16eea7a8992dd36b39f88`  
		Last Modified: Mon, 18 Oct 2021 22:21:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f06cc2cbb18da705b3065ac5c595df3809a82b8ea5e3763fd8fe50d96590e03`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:03f725eb2e70a25215590328677b3f23e21f5e5a620476f43d3ab036efee3343
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a40ad8d21fe5b8d86077ad0f06de3c91a4b4cffc74c1be70fc259f15054b67`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:40:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:40:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:40:17 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:17 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:40:18 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:40:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:20 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6501ba4a4760252cf7cc02d607ee723591654cc0bb5f52520a6e33dc7a0edc25`  
		Last Modified: Mon, 18 Oct 2021 21:43:12 GMT  
		Size: 6.4 MB (6418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680b385ce15bb20e7ba5ac40667562dec340d2d81461023bdf90c3e3fabbebd`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f199395c417cc0c7e6398feae5d9baf39d65e2e0a7bb70170c70b89e589e8dfe`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1aee83547715d6f96b27af07d2631947e319c0f257cbebfed3719ab3e20529`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc-dind-rootless`

```console
$ docker pull docker@sha256:ab0c2c8440ac1dc57509c31a2ec3a78c22371ca27e0031a6218a98b8256d3a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5f35a22a6237a9d6156de30ff19eb4b4ec21d3efa821475842741240b5eae9df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95244762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11315f1e3d51a31f7e66cc17b2135b89aa716b335c6881d409022365201e821f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 22:19:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:35 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 22:19:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 22:19:36 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:37 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 22:19:37 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 22:19:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:37 GMT
CMD []
# Mon, 18 Oct 2021 22:19:41 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 22:19:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 22:19:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 22:19:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 22:19:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 22:19:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425931fed24edf6259d6a6ddd00725a7195a42dd7bc0b70b0cc18d0d1aaa4396`  
		Last Modified: Mon, 18 Oct 2021 22:21:04 GMT  
		Size: 6.5 MB (6521438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a87d63582576ec7a470e771f6c5d16ff7cb7338024ea93995f04bfb4fe1199f`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9e7e65b6f97a6d64f396fdfbbfdf24802e58a822b16eea7a8992dd36b39f88`  
		Last Modified: Mon, 18 Oct 2021 22:21:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f06cc2cbb18da705b3065ac5c595df3809a82b8ea5e3763fd8fe50d96590e03`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48282e6bb68b3cd85c6888c382ce44c03aac4a0c3ddc81d442dfc72efe84aae`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 1.1 MB (1148742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b3f4f2b7dacb4399397b7cac7bbfd3328746289da0eacacdde2b936a389390`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abe8559ece6fc51061309e75b0be253306e8b9d26e64c2ecf486041a51b52f4`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f177d2e28217b973c3b8bc08c5d5a743e443de5daa815086e05848b46b7db`  
		Last Modified: Mon, 18 Oct 2021 22:21:24 GMT  
		Size: 19.1 MB (19124895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280a62307b878257d2128209fd92a1005e52eddf1a1409ef3770d74fc4122e92`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:036139df2869c66580cf19c3f5e10fbfcdc51e44e4c253dd52461dbaf8756d1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91048708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592281427bbc8f0ac33cd2c8cc861023d89fe8804da4082b826bb8976bf55339`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:40:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:40:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:40:17 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:17 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:40:18 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:40:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:20 GMT
CMD []
# Mon, 18 Oct 2021 21:40:27 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 21:40:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 21:40:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 21:40:33 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 21:40:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 21:40:35 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6501ba4a4760252cf7cc02d607ee723591654cc0bb5f52520a6e33dc7a0edc25`  
		Last Modified: Mon, 18 Oct 2021 21:43:12 GMT  
		Size: 6.4 MB (6418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680b385ce15bb20e7ba5ac40667562dec340d2d81461023bdf90c3e3fabbebd`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f199395c417cc0c7e6398feae5d9baf39d65e2e0a7bb70170c70b89e589e8dfe`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1aee83547715d6f96b27af07d2631947e319c0f257cbebfed3719ab3e20529`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375da3ba74accf4f4e776d8ea0d05c23a13b4b2b720c68351e5a106a84dda6e3`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 1.2 MB (1167846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ac90cf496368c08bead07501a2fb6bcf1be125a482b1ba65545eb127ade900`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1a7298291f6aaebb45b8b88842f7e71ac8c03b3ba86694de07dcba597dce8b`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f92a9eb80f5eb157bb083cbb43ee01b129e3a55ba704b5f14a5e73d3957e05f`  
		Last Modified: Mon, 18 Oct 2021 21:43:32 GMT  
		Size: 21.1 MB (21101330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6559ad5989ef407de45b61e2a3ebc564a674911a70765ee6abc411c6c43b88b2`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc-git`

```console
$ docker pull docker@sha256:cc3f9bbe5f3111b565be5971588af383dc3f0af5088db953e89548bf86629034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-rc-git` - linux; amd64

```console
$ docker pull docker@sha256:9a312d18a857179397f05590a5a79d01cae990cd6f109531cd3e49927cc2aa1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75073484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b277ed5b68b1876f78b93b46469cd70d928e03a4a7b69f90957887610a34929`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311f920a717205e58d36759e3188b044daa8b262ce430ae217b6fb94806b5f61`  
		Last Modified: Mon, 18 Oct 2021 22:21:39 GMT  
		Size: 6.6 MB (6630410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a85ba73189c3335850cce7608bd089cdcad6cb0c6131187d644f6d17f6ec6eac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69093629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638acbdc55fc536c4148cdf061e5ea335d61c5db1d7d75a467d1c96babf85bcb`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:42 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a7843f30ad6a2fa274b0b141d4ddbf161ab3f789f4de5d6f2132dba26513b8`  
		Last Modified: Mon, 18 Oct 2021 21:43:47 GMT  
		Size: 6.7 MB (6739047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc-windowsservercore`

```console
$ docker pull docker@sha256:d125ea7479d2d64ebfaf3c09e13c9a2779a138418349bc84d91ccd10ec86ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10-rc-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:9af1a450bff542c3c59ca59c23baa4ac809b21689a52270f0a1ecb2b7b772b99
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737571068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ab72ca4bd277d8bcbd0c1d4724748ee32af45ec02e98bc29896baa85fa824`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 18 Oct 2021 22:15:32 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:15:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-20.10.10-rc1.zip
# Mon, 18 Oct 2021 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97297e0fe24cb9a67e421adf497357c87598b28b5d697e6fd62149bad943f4e`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9537893fbe0e98b432dae141c797577571249c6087b8f5b15ccaf9405a53d927`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c906a419ea1de003ed54aa6fe1ba09760632f94009f04e08804a630b272c0c`  
		Last Modified: Mon, 18 Oct 2021 22:17:56 GMT  
		Size: 50.9 MB (50900751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:d125ea7479d2d64ebfaf3c09e13c9a2779a138418349bc84d91ccd10ec86ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10-rc-windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:9af1a450bff542c3c59ca59c23baa4ac809b21689a52270f0a1ecb2b7b772b99
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737571068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ab72ca4bd277d8bcbd0c1d4724748ee32af45ec02e98bc29896baa85fa824`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 18 Oct 2021 22:15:32 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:15:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-20.10.10-rc1.zip
# Mon, 18 Oct 2021 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97297e0fe24cb9a67e421adf497357c87598b28b5d697e6fd62149bad943f4e`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9537893fbe0e98b432dae141c797577571249c6087b8f5b15ccaf9405a53d927`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c906a419ea1de003ed54aa6fe1ba09760632f94009f04e08804a630b272c0c`  
		Last Modified: Mon, 18 Oct 2021 22:17:56 GMT  
		Size: 50.9 MB (50900751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-rc1`

```console
$ docker pull docker@sha256:e52651216e0b5ac26e6af91dbf569f071278cead01facbe40f96a2c3f3d4c53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-rc1` - linux; amd64

```console
$ docker pull docker@sha256:c1ae01d9bd863fb2c3c35c34372cae93bfb72f08b8c9b47ea04a1e3a2f1238a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68443074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d11a884b0af0757a193f413afd914f494ce5bfbbaf998f2e328877680d1a513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-rc1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:eab2a4f03c6f78fa775f16495d33d5bd9db312068b14db9caa3b631968f19f57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62354582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd1e6d54b025850351cefe3112edff43a74d0a46d04ad08066c1ba8d7e2ea9d`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-rc1-alpine3.14`

```console
$ docker pull docker@sha256:e52651216e0b5ac26e6af91dbf569f071278cead01facbe40f96a2c3f3d4c53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-rc1-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:c1ae01d9bd863fb2c3c35c34372cae93bfb72f08b8c9b47ea04a1e3a2f1238a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68443074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d11a884b0af0757a193f413afd914f494ce5bfbbaf998f2e328877680d1a513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-rc1-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:eab2a4f03c6f78fa775f16495d33d5bd9db312068b14db9caa3b631968f19f57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62354582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd1e6d54b025850351cefe3112edff43a74d0a46d04ad08066c1ba8d7e2ea9d`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-rc1-dind`

```console
$ docker pull docker@sha256:4891561b3f9b41e4cf68eae73192efb192a92501e1882c7b7b03c40a58efd53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-rc1-dind` - linux; amd64

```console
$ docker pull docker@sha256:2f95928d1f82d2ffb79ef4877800c8490e3c86fecd4b2186e20807f6fd5480f6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74969409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36162799b0039f9f46374d98c63fcb428e69a89cf3f2dd0c766cc6df5d87b32c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 22:19:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:35 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 22:19:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 22:19:36 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:37 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 22:19:37 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 22:19:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425931fed24edf6259d6a6ddd00725a7195a42dd7bc0b70b0cc18d0d1aaa4396`  
		Last Modified: Mon, 18 Oct 2021 22:21:04 GMT  
		Size: 6.5 MB (6521438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a87d63582576ec7a470e771f6c5d16ff7cb7338024ea93995f04bfb4fe1199f`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9e7e65b6f97a6d64f396fdfbbfdf24802e58a822b16eea7a8992dd36b39f88`  
		Last Modified: Mon, 18 Oct 2021 22:21:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f06cc2cbb18da705b3065ac5c595df3809a82b8ea5e3763fd8fe50d96590e03`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-rc1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:03f725eb2e70a25215590328677b3f23e21f5e5a620476f43d3ab036efee3343
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a40ad8d21fe5b8d86077ad0f06de3c91a4b4cffc74c1be70fc259f15054b67`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:40:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:40:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:40:17 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:17 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:40:18 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:40:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:20 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6501ba4a4760252cf7cc02d607ee723591654cc0bb5f52520a6e33dc7a0edc25`  
		Last Modified: Mon, 18 Oct 2021 21:43:12 GMT  
		Size: 6.4 MB (6418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680b385ce15bb20e7ba5ac40667562dec340d2d81461023bdf90c3e3fabbebd`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f199395c417cc0c7e6398feae5d9baf39d65e2e0a7bb70170c70b89e589e8dfe`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1aee83547715d6f96b27af07d2631947e319c0f257cbebfed3719ab3e20529`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-rc1-dind-alpine3.14`

```console
$ docker pull docker@sha256:4891561b3f9b41e4cf68eae73192efb192a92501e1882c7b7b03c40a58efd53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-rc1-dind-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:2f95928d1f82d2ffb79ef4877800c8490e3c86fecd4b2186e20807f6fd5480f6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74969409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36162799b0039f9f46374d98c63fcb428e69a89cf3f2dd0c766cc6df5d87b32c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 22:19:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:35 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 22:19:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 22:19:36 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:37 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 22:19:37 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 22:19:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425931fed24edf6259d6a6ddd00725a7195a42dd7bc0b70b0cc18d0d1aaa4396`  
		Last Modified: Mon, 18 Oct 2021 22:21:04 GMT  
		Size: 6.5 MB (6521438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a87d63582576ec7a470e771f6c5d16ff7cb7338024ea93995f04bfb4fe1199f`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9e7e65b6f97a6d64f396fdfbbfdf24802e58a822b16eea7a8992dd36b39f88`  
		Last Modified: Mon, 18 Oct 2021 22:21:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f06cc2cbb18da705b3065ac5c595df3809a82b8ea5e3763fd8fe50d96590e03`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-rc1-dind-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:03f725eb2e70a25215590328677b3f23e21f5e5a620476f43d3ab036efee3343
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a40ad8d21fe5b8d86077ad0f06de3c91a4b4cffc74c1be70fc259f15054b67`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:40:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:40:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:40:17 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:17 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:40:18 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:40:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:20 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6501ba4a4760252cf7cc02d607ee723591654cc0bb5f52520a6e33dc7a0edc25`  
		Last Modified: Mon, 18 Oct 2021 21:43:12 GMT  
		Size: 6.4 MB (6418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680b385ce15bb20e7ba5ac40667562dec340d2d81461023bdf90c3e3fabbebd`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f199395c417cc0c7e6398feae5d9baf39d65e2e0a7bb70170c70b89e589e8dfe`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1aee83547715d6f96b27af07d2631947e319c0f257cbebfed3719ab3e20529`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-rc1-dind-rootless`

```console
$ docker pull docker@sha256:ab0c2c8440ac1dc57509c31a2ec3a78c22371ca27e0031a6218a98b8256d3a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-rc1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5f35a22a6237a9d6156de30ff19eb4b4ec21d3efa821475842741240b5eae9df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95244762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11315f1e3d51a31f7e66cc17b2135b89aa716b335c6881d409022365201e821f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 22:19:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:35 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 22:19:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 22:19:36 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:37 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 22:19:37 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 22:19:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:37 GMT
CMD []
# Mon, 18 Oct 2021 22:19:41 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 22:19:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 22:19:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 22:19:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 22:19:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 22:19:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425931fed24edf6259d6a6ddd00725a7195a42dd7bc0b70b0cc18d0d1aaa4396`  
		Last Modified: Mon, 18 Oct 2021 22:21:04 GMT  
		Size: 6.5 MB (6521438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a87d63582576ec7a470e771f6c5d16ff7cb7338024ea93995f04bfb4fe1199f`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9e7e65b6f97a6d64f396fdfbbfdf24802e58a822b16eea7a8992dd36b39f88`  
		Last Modified: Mon, 18 Oct 2021 22:21:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f06cc2cbb18da705b3065ac5c595df3809a82b8ea5e3763fd8fe50d96590e03`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48282e6bb68b3cd85c6888c382ce44c03aac4a0c3ddc81d442dfc72efe84aae`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 1.1 MB (1148742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b3f4f2b7dacb4399397b7cac7bbfd3328746289da0eacacdde2b936a389390`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abe8559ece6fc51061309e75b0be253306e8b9d26e64c2ecf486041a51b52f4`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f177d2e28217b973c3b8bc08c5d5a743e443de5daa815086e05848b46b7db`  
		Last Modified: Mon, 18 Oct 2021 22:21:24 GMT  
		Size: 19.1 MB (19124895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280a62307b878257d2128209fd92a1005e52eddf1a1409ef3770d74fc4122e92`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-rc1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:036139df2869c66580cf19c3f5e10fbfcdc51e44e4c253dd52461dbaf8756d1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91048708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592281427bbc8f0ac33cd2c8cc861023d89fe8804da4082b826bb8976bf55339`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:40:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:40:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:40:17 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:17 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:40:18 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:40:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:20 GMT
CMD []
# Mon, 18 Oct 2021 21:40:27 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 21:40:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 21:40:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 21:40:33 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 21:40:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 21:40:35 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6501ba4a4760252cf7cc02d607ee723591654cc0bb5f52520a6e33dc7a0edc25`  
		Last Modified: Mon, 18 Oct 2021 21:43:12 GMT  
		Size: 6.4 MB (6418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680b385ce15bb20e7ba5ac40667562dec340d2d81461023bdf90c3e3fabbebd`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f199395c417cc0c7e6398feae5d9baf39d65e2e0a7bb70170c70b89e589e8dfe`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1aee83547715d6f96b27af07d2631947e319c0f257cbebfed3719ab3e20529`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375da3ba74accf4f4e776d8ea0d05c23a13b4b2b720c68351e5a106a84dda6e3`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 1.2 MB (1167846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ac90cf496368c08bead07501a2fb6bcf1be125a482b1ba65545eb127ade900`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1a7298291f6aaebb45b8b88842f7e71ac8c03b3ba86694de07dcba597dce8b`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f92a9eb80f5eb157bb083cbb43ee01b129e3a55ba704b5f14a5e73d3957e05f`  
		Last Modified: Mon, 18 Oct 2021 21:43:32 GMT  
		Size: 21.1 MB (21101330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6559ad5989ef407de45b61e2a3ebc564a674911a70765ee6abc411c6c43b88b2`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-rc1-git`

```console
$ docker pull docker@sha256:cc3f9bbe5f3111b565be5971588af383dc3f0af5088db953e89548bf86629034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-rc1-git` - linux; amd64

```console
$ docker pull docker@sha256:9a312d18a857179397f05590a5a79d01cae990cd6f109531cd3e49927cc2aa1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75073484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b277ed5b68b1876f78b93b46469cd70d928e03a4a7b69f90957887610a34929`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311f920a717205e58d36759e3188b044daa8b262ce430ae217b6fb94806b5f61`  
		Last Modified: Mon, 18 Oct 2021 22:21:39 GMT  
		Size: 6.6 MB (6630410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.10-rc1-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a85ba73189c3335850cce7608bd089cdcad6cb0c6131187d644f6d17f6ec6eac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69093629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638acbdc55fc536c4148cdf061e5ea335d61c5db1d7d75a467d1c96babf85bcb`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:42 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a7843f30ad6a2fa274b0b141d4ddbf161ab3f789f4de5d6f2132dba26513b8`  
		Last Modified: Mon, 18 Oct 2021 21:43:47 GMT  
		Size: 6.7 MB (6739047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-rc1-windowsservercore`

```console
$ docker pull docker@sha256:d125ea7479d2d64ebfaf3c09e13c9a2779a138418349bc84d91ccd10ec86ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10.10-rc1-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:9af1a450bff542c3c59ca59c23baa4ac809b21689a52270f0a1ecb2b7b772b99
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737571068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ab72ca4bd277d8bcbd0c1d4724748ee32af45ec02e98bc29896baa85fa824`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 18 Oct 2021 22:15:32 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:15:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-20.10.10-rc1.zip
# Mon, 18 Oct 2021 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97297e0fe24cb9a67e421adf497357c87598b28b5d697e6fd62149bad943f4e`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9537893fbe0e98b432dae141c797577571249c6087b8f5b15ccaf9405a53d927`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c906a419ea1de003ed54aa6fe1ba09760632f94009f04e08804a630b272c0c`  
		Last Modified: Mon, 18 Oct 2021 22:17:56 GMT  
		Size: 50.9 MB (50900751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-rc1-windowsservercore-1809`

```console
$ docker pull docker@sha256:d125ea7479d2d64ebfaf3c09e13c9a2779a138418349bc84d91ccd10ec86ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10.10-rc1-windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:9af1a450bff542c3c59ca59c23baa4ac809b21689a52270f0a1ecb2b7b772b99
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737571068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ab72ca4bd277d8bcbd0c1d4724748ee32af45ec02e98bc29896baa85fa824`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 18 Oct 2021 22:15:32 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:15:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-20.10.10-rc1.zip
# Mon, 18 Oct 2021 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97297e0fe24cb9a67e421adf497357c87598b28b5d697e6fd62149bad943f4e`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9537893fbe0e98b432dae141c797577571249c6087b8f5b15ccaf9405a53d927`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c906a419ea1de003ed54aa6fe1ba09760632f94009f04e08804a630b272c0c`  
		Last Modified: Mon, 18 Oct 2021 22:17:56 GMT  
		Size: 50.9 MB (50900751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9`

```console
$ docker pull docker@sha256:938bcb85cf77db2b80d219abd5a1424ec15ce11a3adaea6423fa16cc9acfe926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1710b19ecaa7eba8537ea64a35ddec333ff128cda5f2f19b7c4cd6e3a4e0daf7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c324afd4ac0437589f8f6e825c2fed8ef663773f55ac7c8e85cd589f554239d`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-alpine3.14`

```console
$ docker pull docker@sha256:938bcb85cf77db2b80d219abd5a1424ec15ce11a3adaea6423fa16cc9acfe926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1710b19ecaa7eba8537ea64a35ddec333ff128cda5f2f19b7c4cd6e3a4e0daf7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c324afd4ac0437589f8f6e825c2fed8ef663773f55ac7c8e85cd589f554239d`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-dind`

```console
$ docker pull docker@sha256:d842418d21545fde57c2512681d9bdc4ce0e54f2e0305a293ee20a9b6166932b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-dind` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3ba0867a449ca78b731e3251ddeb677fa893dc500293ab0e303a8188b9e4d106
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6144797d483747bee375b8607893579ff8b6d6ff47e83b10ed4827e4123f549e`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:09 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:41:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:41:12 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:41:12 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:41:13 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:41:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:41:15 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8bdd67624c83a9918b7d0bb7d24f84d32a306b3453ac55e213380ee17335d`  
		Last Modified: Mon, 18 Oct 2021 21:44:31 GMT  
		Size: 6.4 MB (6418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e9de043d240e7a3e0baf2f1a9bd6bd1da52fd1a1df9db1d97b50b294c98b8`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b746a27963c477864e414004aab19efff02e763e88444128d5bbf735410a4f`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f756b76c3b8328ed61cc3fef72a62229860b3a7fefcc6e94edda353b7d3a`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-dind-alpine3.14`

```console
$ docker pull docker@sha256:d842418d21545fde57c2512681d9bdc4ce0e54f2e0305a293ee20a9b6166932b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-dind-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-dind-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3ba0867a449ca78b731e3251ddeb677fa893dc500293ab0e303a8188b9e4d106
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6144797d483747bee375b8607893579ff8b6d6ff47e83b10ed4827e4123f549e`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:09 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:41:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:41:12 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:41:12 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:41:13 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:41:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:41:15 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8bdd67624c83a9918b7d0bb7d24f84d32a306b3453ac55e213380ee17335d`  
		Last Modified: Mon, 18 Oct 2021 21:44:31 GMT  
		Size: 6.4 MB (6418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e9de043d240e7a3e0baf2f1a9bd6bd1da52fd1a1df9db1d97b50b294c98b8`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b746a27963c477864e414004aab19efff02e763e88444128d5bbf735410a4f`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f756b76c3b8328ed61cc3fef72a62229860b3a7fefcc6e94edda353b7d3a`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-dind-rootless`

```console
$ docker pull docker@sha256:51cd937b2ad1a1d32179f2e9acc01ea46d4e127cdaf493a533172b1fb019af15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:75acfc77a83d9b4d557aab529432058b78ac6d629325c9d61c385cd2fc48fe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95235937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4aec2427ffe9836431bca031ae4354053a010dae4736917b174d52da90dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
# Tue, 05 Oct 2021 17:32:44 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Oct 2021 17:32:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Oct 2021 17:32:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Oct 2021 17:32:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Oct 2021 17:32:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Oct 2021 17:32:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f850bf44d36d532f71a72ed317e54531b904953d99821dd316e73e777d23c`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.1 MB (1148745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03facf1a1e41afef60e2e7bad46f0fbd44f5b2b3a3328337c3e0a6049120dd8`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919e685bb3723d38cd895248bb1c99de9588af3aba7f57ef5cb72eca54106a9`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79573e4e685e01787d1e021ea1cecb99cdbf78577b160037c6ed2c7f8f2b304`  
		Last Modified: Tue, 05 Oct 2021 17:34:11 GMT  
		Size: 19.1 MB (19118054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7054ab8c007ff95ebed9750aae6c97b9f692ed317ea464234611c57db8601634`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:eb9feb96a9c979384276b169446b5134c441625461108344fde1f18fdee9ce75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91045261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a26cf3ffc31a4748452e2da3ca2a290c3354e441650e7617aaf4a9fbf6d1750`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:09 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:41:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:41:12 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:41:12 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:41:13 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:41:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:41:15 GMT
CMD []
# Mon, 18 Oct 2021 21:41:23 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 21:41:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 21:41:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 21:41:29 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 21:41:30 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 21:41:31 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8bdd67624c83a9918b7d0bb7d24f84d32a306b3453ac55e213380ee17335d`  
		Last Modified: Mon, 18 Oct 2021 21:44:31 GMT  
		Size: 6.4 MB (6418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e9de043d240e7a3e0baf2f1a9bd6bd1da52fd1a1df9db1d97b50b294c98b8`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b746a27963c477864e414004aab19efff02e763e88444128d5bbf735410a4f`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f756b76c3b8328ed61cc3fef72a62229860b3a7fefcc6e94edda353b7d3a`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da73c72dcad0b534b2f4febbace9688a2f4a30bf46b188501e200b3be5977b03`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 1.2 MB (1167836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ff4316d7dcf66341a4e5a7a7519ed9d36f902bb95d2169ebc26549a0f95849`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba611fb139d8c880c857badbc205cee357e35952ae811c52e90139e68f959d57`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098b6fcc42aecdd56305fc4ceba9415e977d589f359ff58a7ee2c72612859ce9`  
		Last Modified: Mon, 18 Oct 2021 21:44:55 GMT  
		Size: 21.1 MB (21096004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeef11aee822059479265f63f55446205a437ef50e49fbfb586c607571b58574`  
		Last Modified: Mon, 18 Oct 2021 21:44:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-git`

```console
$ docker pull docker@sha256:370cbd65cbf44658bc2ce46c8b606213d9e3e3ea04a7d53a0243d67ca6db95aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-git` - linux; amd64

```console
$ docker pull docker@sha256:3bf13c54edb2a2b817bcad4ae459bf6d8b867930b5026d1f51d4593f598495fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75071530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed61dfae734a45e9440fbd932eeb2b244f0079a45398e33dd1478f62a4f3be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:54 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e22895e9057604af4145b328a599ef34ed98eee9085de276ad33fe1adf50f5f`  
		Last Modified: Tue, 05 Oct 2021 17:34:29 GMT  
		Size: 6.6 MB (6630406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6f7fe91a5a952fb482822be280a9c17313785627cdf33330c1980bf4404d6787
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69095577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1ae00454f4fd0beeab581baa00fe5961ae9b97bae5802e58bc1d0e49636a41`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:38 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae700626b8f4a7301ee4ec15808eb5b1b281fa56ecf42eb4a653b7f0b2a5f722`  
		Last Modified: Mon, 18 Oct 2021 21:45:15 GMT  
		Size: 6.7 MB (6739077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-windowsservercore`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10.9-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-windowsservercore-1809`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10.9-windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:d842418d21545fde57c2512681d9bdc4ce0e54f2e0305a293ee20a9b6166932b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3ba0867a449ca78b731e3251ddeb677fa893dc500293ab0e303a8188b9e4d106
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6144797d483747bee375b8607893579ff8b6d6ff47e83b10ed4827e4123f549e`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:09 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:41:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:41:12 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:41:12 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:41:13 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:41:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:41:15 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8bdd67624c83a9918b7d0bb7d24f84d32a306b3453ac55e213380ee17335d`  
		Last Modified: Mon, 18 Oct 2021 21:44:31 GMT  
		Size: 6.4 MB (6418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e9de043d240e7a3e0baf2f1a9bd6bd1da52fd1a1df9db1d97b50b294c98b8`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b746a27963c477864e414004aab19efff02e763e88444128d5bbf735410a4f`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f756b76c3b8328ed61cc3fef72a62229860b3a7fefcc6e94edda353b7d3a`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:51cd937b2ad1a1d32179f2e9acc01ea46d4e127cdaf493a533172b1fb019af15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:75acfc77a83d9b4d557aab529432058b78ac6d629325c9d61c385cd2fc48fe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95235937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4aec2427ffe9836431bca031ae4354053a010dae4736917b174d52da90dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
# Tue, 05 Oct 2021 17:32:44 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Oct 2021 17:32:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Oct 2021 17:32:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Oct 2021 17:32:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Oct 2021 17:32:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Oct 2021 17:32:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f850bf44d36d532f71a72ed317e54531b904953d99821dd316e73e777d23c`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.1 MB (1148745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03facf1a1e41afef60e2e7bad46f0fbd44f5b2b3a3328337c3e0a6049120dd8`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919e685bb3723d38cd895248bb1c99de9588af3aba7f57ef5cb72eca54106a9`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79573e4e685e01787d1e021ea1cecb99cdbf78577b160037c6ed2c7f8f2b304`  
		Last Modified: Tue, 05 Oct 2021 17:34:11 GMT  
		Size: 19.1 MB (19118054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7054ab8c007ff95ebed9750aae6c97b9f692ed317ea464234611c57db8601634`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:eb9feb96a9c979384276b169446b5134c441625461108344fde1f18fdee9ce75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91045261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a26cf3ffc31a4748452e2da3ca2a290c3354e441650e7617aaf4a9fbf6d1750`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:41:08 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:09 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:41:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:41:12 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:41:12 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:41:13 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:41:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:41:15 GMT
CMD []
# Mon, 18 Oct 2021 21:41:23 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 21:41:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 21:41:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:41:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 21:41:29 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 21:41:30 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 21:41:31 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8bdd67624c83a9918b7d0bb7d24f84d32a306b3453ac55e213380ee17335d`  
		Last Modified: Mon, 18 Oct 2021 21:44:31 GMT  
		Size: 6.4 MB (6418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e9de043d240e7a3e0baf2f1a9bd6bd1da52fd1a1df9db1d97b50b294c98b8`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b746a27963c477864e414004aab19efff02e763e88444128d5bbf735410a4f`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f756b76c3b8328ed61cc3fef72a62229860b3a7fefcc6e94edda353b7d3a`  
		Last Modified: Mon, 18 Oct 2021 21:44:30 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da73c72dcad0b534b2f4febbace9688a2f4a30bf46b188501e200b3be5977b03`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 1.2 MB (1167836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ff4316d7dcf66341a4e5a7a7519ed9d36f902bb95d2169ebc26549a0f95849`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba611fb139d8c880c857badbc205cee357e35952ae811c52e90139e68f959d57`  
		Last Modified: Mon, 18 Oct 2021 21:44:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098b6fcc42aecdd56305fc4ceba9415e977d589f359ff58a7ee2c72612859ce9`  
		Last Modified: Mon, 18 Oct 2021 21:44:55 GMT  
		Size: 21.1 MB (21096004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeef11aee822059479265f63f55446205a437ef50e49fbfb586c607571b58574`  
		Last Modified: Mon, 18 Oct 2021 21:44:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:370cbd65cbf44658bc2ce46c8b606213d9e3e3ea04a7d53a0243d67ca6db95aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:3bf13c54edb2a2b817bcad4ae459bf6d8b867930b5026d1f51d4593f598495fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75071530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed61dfae734a45e9440fbd932eeb2b244f0079a45398e33dd1478f62a4f3be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:54 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e22895e9057604af4145b328a599ef34ed98eee9085de276ad33fe1adf50f5f`  
		Last Modified: Tue, 05 Oct 2021 17:34:29 GMT  
		Size: 6.6 MB (6630406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6f7fe91a5a952fb482822be280a9c17313785627cdf33330c1980bf4404d6787
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69095577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1ae00454f4fd0beeab581baa00fe5961ae9b97bae5802e58bc1d0e49636a41`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:41:38 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae700626b8f4a7301ee4ec15808eb5b1b281fa56ecf42eb4a653b7f0b2a5f722`  
		Last Modified: Mon, 18 Oct 2021 21:45:15 GMT  
		Size: 6.7 MB (6739077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:938bcb85cf77db2b80d219abd5a1424ec15ce11a3adaea6423fa16cc9acfe926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1710b19ecaa7eba8537ea64a35ddec333ff128cda5f2f19b7c4cd6e3a4e0daf7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c324afd4ac0437589f8f6e825c2fed8ef663773f55ac7c8e85cd589f554239d`
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
# Mon, 18 Oct 2021 21:40:48 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 18 Oct 2021 21:40:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:59 GMT
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
	-	`sha256:9b2bacb27c3d6ff01f6e8f051e37ec17341cc7fbc76073dea248afcf223aba5d`  
		Last Modified: Mon, 18 Oct 2021 21:44:10 GMT  
		Size: 57.7 MB (57733379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79bdbfa9a5540080db6017b27b917e7c21fbf947abefb068a974a0b55d481e`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a13bdd3b1cef3426a41cadec19b55904b133d95c31c10574f56b0419a93f72`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb034e6582742a188487a0bdde846bf28e29179005b5f423b7d465a2c4e368df`  
		Last Modified: Mon, 18 Oct 2021 21:44:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc`

```console
$ docker pull docker@sha256:e52651216e0b5ac26e6af91dbf569f071278cead01facbe40f96a2c3f3d4c53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:c1ae01d9bd863fb2c3c35c34372cae93bfb72f08b8c9b47ea04a1e3a2f1238a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68443074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d11a884b0af0757a193f413afd914f494ce5bfbbaf998f2e328877680d1a513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:eab2a4f03c6f78fa775f16495d33d5bd9db312068b14db9caa3b631968f19f57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62354582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd1e6d54b025850351cefe3112edff43a74d0a46d04ad08066c1ba8d7e2ea9d`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-dind`

```console
$ docker pull docker@sha256:4891561b3f9b41e4cf68eae73192efb192a92501e1882c7b7b03c40a58efd53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:2f95928d1f82d2ffb79ef4877800c8490e3c86fecd4b2186e20807f6fd5480f6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74969409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36162799b0039f9f46374d98c63fcb428e69a89cf3f2dd0c766cc6df5d87b32c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 22:19:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:35 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 22:19:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 22:19:36 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:37 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 22:19:37 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 22:19:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425931fed24edf6259d6a6ddd00725a7195a42dd7bc0b70b0cc18d0d1aaa4396`  
		Last Modified: Mon, 18 Oct 2021 22:21:04 GMT  
		Size: 6.5 MB (6521438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a87d63582576ec7a470e771f6c5d16ff7cb7338024ea93995f04bfb4fe1199f`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9e7e65b6f97a6d64f396fdfbbfdf24802e58a822b16eea7a8992dd36b39f88`  
		Last Modified: Mon, 18 Oct 2021 22:21:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f06cc2cbb18da705b3065ac5c595df3809a82b8ea5e3763fd8fe50d96590e03`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:03f725eb2e70a25215590328677b3f23e21f5e5a620476f43d3ab036efee3343
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a40ad8d21fe5b8d86077ad0f06de3c91a4b4cffc74c1be70fc259f15054b67`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:40:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:40:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:40:17 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:17 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:40:18 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:40:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:20 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6501ba4a4760252cf7cc02d607ee723591654cc0bb5f52520a6e33dc7a0edc25`  
		Last Modified: Mon, 18 Oct 2021 21:43:12 GMT  
		Size: 6.4 MB (6418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680b385ce15bb20e7ba5ac40667562dec340d2d81461023bdf90c3e3fabbebd`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f199395c417cc0c7e6398feae5d9baf39d65e2e0a7bb70170c70b89e589e8dfe`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1aee83547715d6f96b27af07d2631947e319c0f257cbebfed3719ab3e20529`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:ab0c2c8440ac1dc57509c31a2ec3a78c22371ca27e0031a6218a98b8256d3a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5f35a22a6237a9d6156de30ff19eb4b4ec21d3efa821475842741240b5eae9df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95244762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11315f1e3d51a31f7e66cc17b2135b89aa716b335c6881d409022365201e821f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 22:19:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:35 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 22:19:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 22:19:36 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:37 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 22:19:37 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 22:19:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:37 GMT
CMD []
# Mon, 18 Oct 2021 22:19:41 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 22:19:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 22:19:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 22:19:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 22:19:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 22:19:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 22:19:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425931fed24edf6259d6a6ddd00725a7195a42dd7bc0b70b0cc18d0d1aaa4396`  
		Last Modified: Mon, 18 Oct 2021 22:21:04 GMT  
		Size: 6.5 MB (6521438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a87d63582576ec7a470e771f6c5d16ff7cb7338024ea93995f04bfb4fe1199f`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9e7e65b6f97a6d64f396fdfbbfdf24802e58a822b16eea7a8992dd36b39f88`  
		Last Modified: Mon, 18 Oct 2021 22:21:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f06cc2cbb18da705b3065ac5c595df3809a82b8ea5e3763fd8fe50d96590e03`  
		Last Modified: Mon, 18 Oct 2021 22:21:02 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48282e6bb68b3cd85c6888c382ce44c03aac4a0c3ddc81d442dfc72efe84aae`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 1.1 MB (1148742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b3f4f2b7dacb4399397b7cac7bbfd3328746289da0eacacdde2b936a389390`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abe8559ece6fc51061309e75b0be253306e8b9d26e64c2ecf486041a51b52f4`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f177d2e28217b973c3b8bc08c5d5a743e443de5daa815086e05848b46b7db`  
		Last Modified: Mon, 18 Oct 2021 22:21:24 GMT  
		Size: 19.1 MB (19124895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280a62307b878257d2128209fd92a1005e52eddf1a1409ef3770d74fc4122e92`  
		Last Modified: Mon, 18 Oct 2021 22:21:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:036139df2869c66580cf19c3f5e10fbfcdc51e44e4c253dd52461dbaf8756d1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91048708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592281427bbc8f0ac33cd2c8cc861023d89fe8804da4082b826bb8976bf55339`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Oct 2021 21:40:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Oct 2021 21:40:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Oct 2021 21:40:17 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:17 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Oct 2021 21:40:18 GMT
EXPOSE 2375 2376
# Mon, 18 Oct 2021 21:40:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:20 GMT
CMD []
# Mon, 18 Oct 2021 21:40:27 GMT
RUN apk add --no-cache iproute2
# Mon, 18 Oct 2021 21:40:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Oct 2021 21:40:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Oct 2021 21:40:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Oct 2021 21:40:33 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Oct 2021 21:40:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Oct 2021 21:40:35 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6501ba4a4760252cf7cc02d607ee723591654cc0bb5f52520a6e33dc7a0edc25`  
		Last Modified: Mon, 18 Oct 2021 21:43:12 GMT  
		Size: 6.4 MB (6418461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680b385ce15bb20e7ba5ac40667562dec340d2d81461023bdf90c3e3fabbebd`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f199395c417cc0c7e6398feae5d9baf39d65e2e0a7bb70170c70b89e589e8dfe`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1aee83547715d6f96b27af07d2631947e319c0f257cbebfed3719ab3e20529`  
		Last Modified: Mon, 18 Oct 2021 21:43:10 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375da3ba74accf4f4e776d8ea0d05c23a13b4b2b720c68351e5a106a84dda6e3`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 1.2 MB (1167846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ac90cf496368c08bead07501a2fb6bcf1be125a482b1ba65545eb127ade900`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1a7298291f6aaebb45b8b88842f7e71ac8c03b3ba86694de07dcba597dce8b`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f92a9eb80f5eb157bb083cbb43ee01b129e3a55ba704b5f14a5e73d3957e05f`  
		Last Modified: Mon, 18 Oct 2021 21:43:32 GMT  
		Size: 21.1 MB (21101330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6559ad5989ef407de45b61e2a3ebc564a674911a70765ee6abc411c6c43b88b2`  
		Last Modified: Mon, 18 Oct 2021 21:43:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-git`

```console
$ docker pull docker@sha256:cc3f9bbe5f3111b565be5971588af383dc3f0af5088db953e89548bf86629034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-git` - linux; amd64

```console
$ docker pull docker@sha256:9a312d18a857179397f05590a5a79d01cae990cd6f109531cd3e49927cc2aa1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75073484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b277ed5b68b1876f78b93b46469cd70d928e03a4a7b69f90957887610a34929`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Oct 2021 22:19:21 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:19:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 22:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 22:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 22:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 22:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 22:19:29 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 22:19:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfef21a1ba86a2a49122b42c2b6894a1fb8b832279017d10fcf3799e95d5f0`  
		Last Modified: Mon, 18 Oct 2021 22:20:47 GMT  
		Size: 63.7 MB (63691665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ed9bdac873af3eff9398dbc77b000df4a4c25ef3a78ced87e178ff1c92645`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51846a1759acabeb7964b68eb7c183c0668a5ff1175ac9b1952fc4949b649cf`  
		Last Modified: Mon, 18 Oct 2021 22:20:36 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ab21c0404cdc3f3a67b807ff478d3a3d705a4a37c4bc9e3b922ca8e984a2fd`  
		Last Modified: Mon, 18 Oct 2021 22:20:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311f920a717205e58d36759e3188b044daa8b262ce430ae217b6fb94806b5f61`  
		Last Modified: Mon, 18 Oct 2021 22:21:39 GMT  
		Size: 6.6 MB (6630410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a85ba73189c3335850cce7608bd089cdcad6cb0c6131187d644f6d17f6ec6eac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69093629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638acbdc55fc536c4148cdf061e5ea335d61c5db1d7d75a467d1c96babf85bcb`
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
# Mon, 18 Oct 2021 21:39:53 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 21:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.10-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.10-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.10-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.10-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Oct 2021 21:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Oct 2021 21:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Oct 2021 21:40:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Oct 2021 21:40:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:40:04 GMT
CMD ["sh"]
# Mon, 18 Oct 2021 21:40:42 GMT
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
	-	`sha256:112f3374d6fabbfe7b2c992c077ac3658ff8d061a8e18265257b45cd60739c0d`  
		Last Modified: Mon, 18 Oct 2021 21:42:54 GMT  
		Size: 57.7 MB (57731459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffe46428f8f4e7d13099151a78aa124e254522444b80d46bcec4e3e3fc41eb`  
		Last Modified: Mon, 18 Oct 2021 21:42:44 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699487bf567a986ddfb631b8655b487e6922d4a86ee9ff17b738d32ae342fa7`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f64888be82e82dc404000ef04193fab09949191aa4a5abd16eb3f76de6422`  
		Last Modified: Mon, 18 Oct 2021 21:42:45 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a7843f30ad6a2fa274b0b141d4ddbf161ab3f789f4de5d6f2132dba26513b8`  
		Last Modified: Mon, 18 Oct 2021 21:43:47 GMT  
		Size: 6.7 MB (6739047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:d125ea7479d2d64ebfaf3c09e13c9a2779a138418349bc84d91ccd10ec86ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:rc-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:9af1a450bff542c3c59ca59c23baa4ac809b21689a52270f0a1ecb2b7b772b99
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737571068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ab72ca4bd277d8bcbd0c1d4724748ee32af45ec02e98bc29896baa85fa824`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 18 Oct 2021 22:15:32 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:15:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-20.10.10-rc1.zip
# Mon, 18 Oct 2021 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97297e0fe24cb9a67e421adf497357c87598b28b5d697e6fd62149bad943f4e`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9537893fbe0e98b432dae141c797577571249c6087b8f5b15ccaf9405a53d927`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c906a419ea1de003ed54aa6fe1ba09760632f94009f04e08804a630b272c0c`  
		Last Modified: Mon, 18 Oct 2021 22:17:56 GMT  
		Size: 50.9 MB (50900751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:d125ea7479d2d64ebfaf3c09e13c9a2779a138418349bc84d91ccd10ec86ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:9af1a450bff542c3c59ca59c23baa4ac809b21689a52270f0a1ecb2b7b772b99
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737571068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ab72ca4bd277d8bcbd0c1d4724748ee32af45ec02e98bc29896baa85fa824`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 18 Oct 2021 22:15:32 GMT
ENV DOCKER_VERSION=20.10.10-rc1
# Mon, 18 Oct 2021 22:15:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-20.10.10-rc1.zip
# Mon, 18 Oct 2021 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97297e0fe24cb9a67e421adf497357c87598b28b5d697e6fd62149bad943f4e`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9537893fbe0e98b432dae141c797577571249c6087b8f5b15ccaf9405a53d927`  
		Last Modified: Mon, 18 Oct 2021 22:17:44 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c906a419ea1de003ed54aa6fe1ba09760632f94009f04e08804a630b272c0c`  
		Last Modified: Mon, 18 Oct 2021 22:17:56 GMT  
		Size: 50.9 MB (50900751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
