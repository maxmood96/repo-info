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
$ docker pull docker@sha256:38230c67d2c744407d71324a088e390aa7e908a486276de9c9c22e69004ad159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:fdc0b6674a4b32fc9e8a96289c20fb4a8b1f5cab03c5e26a20e46d7c4157147f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69220694a6d2709ccca28de76e6ccd680247d492f0c285689f75eba4c3fb972b`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
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
$ docker pull docker@sha256:4affae8ac27539b74e27ac4f2d6662902a328340c218336944bab7e482244cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:81e122bb407b639068f161ddb90dd0c0e894b1911b496d114aa83752db7a8a81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74972094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06998f605417d732cd4770de75e71e2157cbd3cfb7485a87b6876d3a80b91817`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 22:19:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:37 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 22:19:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 22:19:38 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:38 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 22:19:38 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 22:19:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:39 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6839fcddb5ee581fd7c146a4dbdc867e1628376fbead0291a71112831ce014a`  
		Last Modified: Mon, 25 Oct 2021 22:20:44 GMT  
		Size: 6.5 MB (6521415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bdc5169f76b30910cf29996b216228ba8307c21b6eff5e28a3bf1fab197af`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ae7ea8d6a96767543b911bb57b6c4c6afa99cf2a5a851646d2da7cddd93e1`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1810ac9c2aaf1b158659b8418ed29c7c2cd58922eb290958f1b44c840838ee`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 2.6 KB (2618 bytes)  
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
$ docker pull docker@sha256:e3b96843078e6e48bed3909684a01b7143259764acdfd18a6700e3bc8bbc54e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ae51a8093d119722c187e20f5d76904bac00e61d325743efc89f94c96170d89b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95247458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe9dea8276ca16e54836a93936cfc08f6cb0c92332a509a11af82cf6279dd`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 22:19:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:37 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 22:19:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 22:19:38 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:38 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 22:19:38 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 22:19:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:39 GMT
CMD []
# Mon, 25 Oct 2021 22:19:43 GMT
RUN apk add --no-cache iproute2
# Mon, 25 Oct 2021 22:19:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 25 Oct 2021 22:19:45 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 25 Oct 2021 22:19:48 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 25 Oct 2021 22:19:48 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 25 Oct 2021 22:19:48 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6839fcddb5ee581fd7c146a4dbdc867e1628376fbead0291a71112831ce014a`  
		Last Modified: Mon, 25 Oct 2021 22:20:44 GMT  
		Size: 6.5 MB (6521415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bdc5169f76b30910cf29996b216228ba8307c21b6eff5e28a3bf1fab197af`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ae7ea8d6a96767543b911bb57b6c4c6afa99cf2a5a851646d2da7cddd93e1`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1810ac9c2aaf1b158659b8418ed29c7c2cd58922eb290958f1b44c840838ee`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39de696ecbe11f889a0e673c4675276493cfcd427e536d768cd2108ceca46594`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 1.1 MB (1148744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a193ebd2c391d47fa93651736bf8b3db0adfa2f2c96815fcd86a6052c08b44c`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f236955e2902b0e3e791b24fd224beb51007c72db8a0bd5f5557727fd58a682`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d00866a1a5518766d11985ee8388e48bfcc7e04b2ea2246fa685a80d8841de`  
		Last Modified: Mon, 25 Oct 2021 22:21:08 GMT  
		Size: 19.1 MB (19124908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b3d92cf825e0a9099b445878e12b1940093c0a3bfc950dcdfd08c608f63c91`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 218.0 B  
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
$ docker pull docker@sha256:e5f54cb9eb9522c267be639dadf83aae67905f403563ed262076bfa3dd2cd044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:9d3f1cf7762bfee22b817ab853d8412afc0821185eae0a20340cc9b6b38e8de0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75076201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36edeffa553a75eeae015925e97cfa57bc864d9a952792ce45adcc9f9195b0d`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:52 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc210962d4edc0ccd66dc34141aeff012a0aa9cdfcd213ed5b5965198653850`  
		Last Modified: Mon, 25 Oct 2021 22:21:26 GMT  
		Size: 6.6 MB (6630419 bytes)  
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
$ docker pull docker@sha256:38230c67d2c744407d71324a088e390aa7e908a486276de9c9c22e69004ad159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:fdc0b6674a4b32fc9e8a96289c20fb4a8b1f5cab03c5e26a20e46d7c4157147f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69220694a6d2709ccca28de76e6ccd680247d492f0c285689f75eba4c3fb972b`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
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
$ docker pull docker@sha256:4affae8ac27539b74e27ac4f2d6662902a328340c218336944bab7e482244cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:81e122bb407b639068f161ddb90dd0c0e894b1911b496d114aa83752db7a8a81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74972094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06998f605417d732cd4770de75e71e2157cbd3cfb7485a87b6876d3a80b91817`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 22:19:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:37 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 22:19:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 22:19:38 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:38 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 22:19:38 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 22:19:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:39 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6839fcddb5ee581fd7c146a4dbdc867e1628376fbead0291a71112831ce014a`  
		Last Modified: Mon, 25 Oct 2021 22:20:44 GMT  
		Size: 6.5 MB (6521415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bdc5169f76b30910cf29996b216228ba8307c21b6eff5e28a3bf1fab197af`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ae7ea8d6a96767543b911bb57b6c4c6afa99cf2a5a851646d2da7cddd93e1`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1810ac9c2aaf1b158659b8418ed29c7c2cd58922eb290958f1b44c840838ee`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 2.6 KB (2618 bytes)  
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
$ docker pull docker@sha256:e3b96843078e6e48bed3909684a01b7143259764acdfd18a6700e3bc8bbc54e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ae51a8093d119722c187e20f5d76904bac00e61d325743efc89f94c96170d89b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95247458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe9dea8276ca16e54836a93936cfc08f6cb0c92332a509a11af82cf6279dd`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 22:19:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:37 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 22:19:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 22:19:38 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:38 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 22:19:38 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 22:19:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:39 GMT
CMD []
# Mon, 25 Oct 2021 22:19:43 GMT
RUN apk add --no-cache iproute2
# Mon, 25 Oct 2021 22:19:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 25 Oct 2021 22:19:45 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 25 Oct 2021 22:19:48 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 25 Oct 2021 22:19:48 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 25 Oct 2021 22:19:48 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6839fcddb5ee581fd7c146a4dbdc867e1628376fbead0291a71112831ce014a`  
		Last Modified: Mon, 25 Oct 2021 22:20:44 GMT  
		Size: 6.5 MB (6521415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bdc5169f76b30910cf29996b216228ba8307c21b6eff5e28a3bf1fab197af`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ae7ea8d6a96767543b911bb57b6c4c6afa99cf2a5a851646d2da7cddd93e1`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1810ac9c2aaf1b158659b8418ed29c7c2cd58922eb290958f1b44c840838ee`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39de696ecbe11f889a0e673c4675276493cfcd427e536d768cd2108ceca46594`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 1.1 MB (1148744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a193ebd2c391d47fa93651736bf8b3db0adfa2f2c96815fcd86a6052c08b44c`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f236955e2902b0e3e791b24fd224beb51007c72db8a0bd5f5557727fd58a682`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d00866a1a5518766d11985ee8388e48bfcc7e04b2ea2246fa685a80d8841de`  
		Last Modified: Mon, 25 Oct 2021 22:21:08 GMT  
		Size: 19.1 MB (19124908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b3d92cf825e0a9099b445878e12b1940093c0a3bfc950dcdfd08c608f63c91`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 218.0 B  
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
$ docker pull docker@sha256:e5f54cb9eb9522c267be639dadf83aae67905f403563ed262076bfa3dd2cd044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:9d3f1cf7762bfee22b817ab853d8412afc0821185eae0a20340cc9b6b38e8de0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75076201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36edeffa553a75eeae015925e97cfa57bc864d9a952792ce45adcc9f9195b0d`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:52 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc210962d4edc0ccd66dc34141aeff012a0aa9cdfcd213ed5b5965198653850`  
		Last Modified: Mon, 25 Oct 2021 22:21:26 GMT  
		Size: 6.6 MB (6630419 bytes)  
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
$ docker pull docker@sha256:38230c67d2c744407d71324a088e390aa7e908a486276de9c9c22e69004ad159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10` - linux; amd64

```console
$ docker pull docker@sha256:fdc0b6674a4b32fc9e8a96289c20fb4a8b1f5cab03c5e26a20e46d7c4157147f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69220694a6d2709ccca28de76e6ccd680247d492f0c285689f75eba4c3fb972b`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
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
$ docker pull docker@sha256:38230c67d2c744407d71324a088e390aa7e908a486276de9c9c22e69004ad159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:fdc0b6674a4b32fc9e8a96289c20fb4a8b1f5cab03c5e26a20e46d7c4157147f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69220694a6d2709ccca28de76e6ccd680247d492f0c285689f75eba4c3fb972b`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
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
$ docker pull docker@sha256:4affae8ac27539b74e27ac4f2d6662902a328340c218336944bab7e482244cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:81e122bb407b639068f161ddb90dd0c0e894b1911b496d114aa83752db7a8a81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74972094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06998f605417d732cd4770de75e71e2157cbd3cfb7485a87b6876d3a80b91817`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 22:19:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:37 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 22:19:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 22:19:38 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:38 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 22:19:38 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 22:19:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:39 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6839fcddb5ee581fd7c146a4dbdc867e1628376fbead0291a71112831ce014a`  
		Last Modified: Mon, 25 Oct 2021 22:20:44 GMT  
		Size: 6.5 MB (6521415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bdc5169f76b30910cf29996b216228ba8307c21b6eff5e28a3bf1fab197af`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ae7ea8d6a96767543b911bb57b6c4c6afa99cf2a5a851646d2da7cddd93e1`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1810ac9c2aaf1b158659b8418ed29c7c2cd58922eb290958f1b44c840838ee`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 2.6 KB (2618 bytes)  
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
$ docker pull docker@sha256:4affae8ac27539b74e27ac4f2d6662902a328340c218336944bab7e482244cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-dind-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:81e122bb407b639068f161ddb90dd0c0e894b1911b496d114aa83752db7a8a81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74972094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06998f605417d732cd4770de75e71e2157cbd3cfb7485a87b6876d3a80b91817`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 22:19:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:37 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 22:19:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 22:19:38 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:38 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 22:19:38 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 22:19:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:39 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6839fcddb5ee581fd7c146a4dbdc867e1628376fbead0291a71112831ce014a`  
		Last Modified: Mon, 25 Oct 2021 22:20:44 GMT  
		Size: 6.5 MB (6521415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bdc5169f76b30910cf29996b216228ba8307c21b6eff5e28a3bf1fab197af`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ae7ea8d6a96767543b911bb57b6c4c6afa99cf2a5a851646d2da7cddd93e1`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1810ac9c2aaf1b158659b8418ed29c7c2cd58922eb290958f1b44c840838ee`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 2.6 KB (2618 bytes)  
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
$ docker pull docker@sha256:e3b96843078e6e48bed3909684a01b7143259764acdfd18a6700e3bc8bbc54e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ae51a8093d119722c187e20f5d76904bac00e61d325743efc89f94c96170d89b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95247458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe9dea8276ca16e54836a93936cfc08f6cb0c92332a509a11af82cf6279dd`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 22:19:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:37 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 22:19:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 22:19:38 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:38 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 22:19:38 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 22:19:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:39 GMT
CMD []
# Mon, 25 Oct 2021 22:19:43 GMT
RUN apk add --no-cache iproute2
# Mon, 25 Oct 2021 22:19:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 25 Oct 2021 22:19:45 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 25 Oct 2021 22:19:48 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 25 Oct 2021 22:19:48 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 25 Oct 2021 22:19:48 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6839fcddb5ee581fd7c146a4dbdc867e1628376fbead0291a71112831ce014a`  
		Last Modified: Mon, 25 Oct 2021 22:20:44 GMT  
		Size: 6.5 MB (6521415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bdc5169f76b30910cf29996b216228ba8307c21b6eff5e28a3bf1fab197af`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ae7ea8d6a96767543b911bb57b6c4c6afa99cf2a5a851646d2da7cddd93e1`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1810ac9c2aaf1b158659b8418ed29c7c2cd58922eb290958f1b44c840838ee`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39de696ecbe11f889a0e673c4675276493cfcd427e536d768cd2108ceca46594`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 1.1 MB (1148744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a193ebd2c391d47fa93651736bf8b3db0adfa2f2c96815fcd86a6052c08b44c`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f236955e2902b0e3e791b24fd224beb51007c72db8a0bd5f5557727fd58a682`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d00866a1a5518766d11985ee8388e48bfcc7e04b2ea2246fa685a80d8841de`  
		Last Modified: Mon, 25 Oct 2021 22:21:08 GMT  
		Size: 19.1 MB (19124908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b3d92cf825e0a9099b445878e12b1940093c0a3bfc950dcdfd08c608f63c91`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 218.0 B  
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
$ docker pull docker@sha256:e5f54cb9eb9522c267be639dadf83aae67905f403563ed262076bfa3dd2cd044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.10-git` - linux; amd64

```console
$ docker pull docker@sha256:9d3f1cf7762bfee22b817ab853d8412afc0821185eae0a20340cc9b6b38e8de0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75076201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36edeffa553a75eeae015925e97cfa57bc864d9a952792ce45adcc9f9195b0d`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:52 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc210962d4edc0ccd66dc34141aeff012a0aa9cdfcd213ed5b5965198653850`  
		Last Modified: Mon, 25 Oct 2021 22:21:26 GMT  
		Size: 6.6 MB (6630419 bytes)  
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
$ docker pull docker@sha256:4affae8ac27539b74e27ac4f2d6662902a328340c218336944bab7e482244cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:81e122bb407b639068f161ddb90dd0c0e894b1911b496d114aa83752db7a8a81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74972094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06998f605417d732cd4770de75e71e2157cbd3cfb7485a87b6876d3a80b91817`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 22:19:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:37 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 22:19:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 22:19:38 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:38 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 22:19:38 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 22:19:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:39 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6839fcddb5ee581fd7c146a4dbdc867e1628376fbead0291a71112831ce014a`  
		Last Modified: Mon, 25 Oct 2021 22:20:44 GMT  
		Size: 6.5 MB (6521415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bdc5169f76b30910cf29996b216228ba8307c21b6eff5e28a3bf1fab197af`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ae7ea8d6a96767543b911bb57b6c4c6afa99cf2a5a851646d2da7cddd93e1`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1810ac9c2aaf1b158659b8418ed29c7c2cd58922eb290958f1b44c840838ee`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 2.6 KB (2618 bytes)  
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
$ docker pull docker@sha256:e3b96843078e6e48bed3909684a01b7143259764acdfd18a6700e3bc8bbc54e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ae51a8093d119722c187e20f5d76904bac00e61d325743efc89f94c96170d89b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95247458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe9dea8276ca16e54836a93936cfc08f6cb0c92332a509a11af82cf6279dd`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 25 Oct 2021 22:19:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:37 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 25 Oct 2021 22:19:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 25 Oct 2021 22:19:38 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:38 GMT
VOLUME [/var/lib/docker]
# Mon, 25 Oct 2021 22:19:38 GMT
EXPOSE 2375 2376
# Mon, 25 Oct 2021 22:19:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:39 GMT
CMD []
# Mon, 25 Oct 2021 22:19:43 GMT
RUN apk add --no-cache iproute2
# Mon, 25 Oct 2021 22:19:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 25 Oct 2021 22:19:45 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 25 Oct 2021 22:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 25 Oct 2021 22:19:48 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 25 Oct 2021 22:19:48 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 25 Oct 2021 22:19:48 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6839fcddb5ee581fd7c146a4dbdc867e1628376fbead0291a71112831ce014a`  
		Last Modified: Mon, 25 Oct 2021 22:20:44 GMT  
		Size: 6.5 MB (6521415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bdc5169f76b30910cf29996b216228ba8307c21b6eff5e28a3bf1fab197af`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ae7ea8d6a96767543b911bb57b6c4c6afa99cf2a5a851646d2da7cddd93e1`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1810ac9c2aaf1b158659b8418ed29c7c2cd58922eb290958f1b44c840838ee`  
		Last Modified: Mon, 25 Oct 2021 22:20:43 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39de696ecbe11f889a0e673c4675276493cfcd427e536d768cd2108ceca46594`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 1.1 MB (1148744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a193ebd2c391d47fa93651736bf8b3db0adfa2f2c96815fcd86a6052c08b44c`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f236955e2902b0e3e791b24fd224beb51007c72db8a0bd5f5557727fd58a682`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d00866a1a5518766d11985ee8388e48bfcc7e04b2ea2246fa685a80d8841de`  
		Last Modified: Mon, 25 Oct 2021 22:21:08 GMT  
		Size: 19.1 MB (19124908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b3d92cf825e0a9099b445878e12b1940093c0a3bfc950dcdfd08c608f63c91`  
		Last Modified: Mon, 25 Oct 2021 22:21:05 GMT  
		Size: 218.0 B  
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
$ docker pull docker@sha256:e5f54cb9eb9522c267be639dadf83aae67905f403563ed262076bfa3dd2cd044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:9d3f1cf7762bfee22b817ab853d8412afc0821185eae0a20340cc9b6b38e8de0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75076201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36edeffa553a75eeae015925e97cfa57bc864d9a952792ce45adcc9f9195b0d`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
CMD ["sh"]
# Mon, 25 Oct 2021 22:19:52 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc210962d4edc0ccd66dc34141aeff012a0aa9cdfcd213ed5b5965198653850`  
		Last Modified: Mon, 25 Oct 2021 22:21:26 GMT  
		Size: 6.6 MB (6630419 bytes)  
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
$ docker pull docker@sha256:38230c67d2c744407d71324a088e390aa7e908a486276de9c9c22e69004ad159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:fdc0b6674a4b32fc9e8a96289c20fb4a8b1f5cab03c5e26a20e46d7c4157147f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69220694a6d2709ccca28de76e6ccd680247d492f0c285689f75eba4c3fb972b`
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
# Mon, 25 Oct 2021 22:19:23 GMT
ENV DOCKER_VERSION=20.10.10
# Mon, 25 Oct 2021 22:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 25 Oct 2021 22:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 25 Oct 2021 22:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 25 Oct 2021 22:19:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 25 Oct 2021 22:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Oct 2021 22:19:30 GMT
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
	-	`sha256:ec4652588449bca1507b708ff4376473e23bd9caae32b961d3d9bd9b5e3257be`  
		Last Modified: Mon, 25 Oct 2021 22:20:25 GMT  
		Size: 63.7 MB (63694371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792da46ddc692987d3e0e571233e14c220e7cf4d61c2827897841a878640038a`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515f90f4bb3b03858dd9d5b7ad7d5fec29caa63a6cb256bdc0d4e06c0fbbff8`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781537e4c928bcb25ad2d3b050a3825e5e9bcfe8de8fd85167e4852ab5e97a53`  
		Last Modified: Mon, 25 Oct 2021 22:20:14 GMT  
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
