## `docker:git`

```console
$ docker pull docker@sha256:3141a9f66a8eaa90e74a0fbf999ab40e7cf3eb2890577ea17e688ead7e020641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:e470d67889af90ea7d5008faaba9f8c6bc43de06304dab2b8b2fdd492eae39d3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76865996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6fefe517a89d818bcbdf3465b0bf9657cc4b3bc72f3cb9bc098ff9169ace33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2019 23:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 11 Dec 2019 23:20:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 11 Dec 2019 23:20:50 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Dec 2019 23:20:50 GMT
ENV DOCKER_VERSION=19.03.5
# Wed, 11 Dec 2019 23:20:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Dec 2019 23:20:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Dec 2019 23:20:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Dec 2019 23:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Dec 2019 23:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Dec 2019 23:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2019 23:20:58 GMT
CMD ["sh"]
# Wed, 11 Dec 2019 23:21:36 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ca718c007e090ea606c06ea2d0625898b7c360306699eb418b690c37a01d3e`  
		Last Modified: Wed, 11 Dec 2019 23:21:50 GMT  
		Size: 2.4 MB (2422634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cec70188224ea7ba22191c00accecaaf1b78e1f4fab18701e028cca51d3def4`  
		Last Modified: Wed, 11 Dec 2019 23:21:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c248f2b1183d8e2e483bf7ae591bba5e4a4acd64f28896ea24ccf2bba09b9df9`  
		Last Modified: Wed, 11 Dec 2019 23:22:01 GMT  
		Size: 63.8 MB (63803076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2503d20971037b9a2d5a7c7ffb0bc2ed815dd4aed7ff70ea8ca55d87b85c2ca`  
		Last Modified: Wed, 11 Dec 2019 23:21:49 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b0d619bd33ab28b4e8fe1717ca1f585c4b8fe378f75dba428d12e1a2363b0c`  
		Last Modified: Wed, 11 Dec 2019 23:21:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec7a6d53674b6e4eb41a4141aa72ac2894d0b720162d4def56525d374de64c5`  
		Last Modified: Wed, 11 Dec 2019 23:21:49 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fedb39903367c1422036ce9ec4d702341b70ad82cc01b6e76bffdc2642b1395`  
		Last Modified: Wed, 11 Dec 2019 23:22:36 GMT  
		Size: 7.9 MB (7851318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v6

```console
$ docker pull docker@sha256:d109033468e4c2d3916676f30f34833313dc39a469c23b24dda9845a940b73af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71863615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1158e8b1b186b886304088df5c4a3e6dd590a351875f2051f206250d4e8ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2019 22:49:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 11 Dec 2019 22:49:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 11 Dec 2019 22:49:39 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Dec 2019 22:49:40 GMT
ENV DOCKER_VERSION=19.03.5
# Wed, 11 Dec 2019 22:49:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Dec 2019 22:49:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Dec 2019 22:49:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Dec 2019 22:49:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Dec 2019 22:49:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Dec 2019 22:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2019 22:49:55 GMT
CMD ["sh"]
# Wed, 11 Dec 2019 22:50:52 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ff5944bdb7e9171cd9a0b4ff982e7f9f76bee3f40ac1a008ca4ef6a3fc27b`  
		Last Modified: Wed, 11 Dec 2019 22:51:15 GMT  
		Size: 2.3 MB (2336234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46de1899c6245f4aa2d837e9f7c82667f72436fcc7f851b6456f00a63952d93`  
		Last Modified: Wed, 11 Dec 2019 22:51:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5467d422b56b61d8e91e846ad852dd7c79cdf05075198258733b2027d5f493c`  
		Last Modified: Wed, 11 Dec 2019 22:51:32 GMT  
		Size: 59.5 MB (59537105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57abdd7b742761c1733281558639e15c8c0451a6ec25fecee23119353c05b73`  
		Last Modified: Wed, 11 Dec 2019 22:51:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8887fef07d0dab5b2fab086bf75186f5d24bc72b9c2e6ffce87a2391007c77cd`  
		Last Modified: Wed, 11 Dec 2019 22:51:12 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ca6e031218cb5b93c4111cfec0b7f769837784da486b8aba989ca6b22acabb`  
		Last Modified: Wed, 11 Dec 2019 22:51:12 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0700c76dc28a7b907870ceaa7e72e7f65265a74a0582be0cfd5713b288d6fdb`  
		Last Modified: Wed, 11 Dec 2019 22:52:01 GMT  
		Size: 7.4 MB (7417097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v7

```console
$ docker pull docker@sha256:81fefdf9037cb7a9b65fc7e76bc4fd79fc3fb2011172b0a47ab4154698bb478a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70735384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84c951058f8f3b2ad0e89f4efb78fe2d0f7458ceb918af47a93fcde708e716c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2019 22:57:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 11 Dec 2019 22:57:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 11 Dec 2019 22:57:45 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Dec 2019 22:57:45 GMT
ENV DOCKER_VERSION=19.03.5
# Wed, 11 Dec 2019 22:57:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Dec 2019 22:57:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Dec 2019 22:57:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Dec 2019 22:57:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Dec 2019 22:57:58 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Dec 2019 22:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2019 22:57:59 GMT
CMD ["sh"]
# Wed, 11 Dec 2019 22:58:29 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d7fa3dbcd1426cadb6cb4b0846f206a8926d14baffbe8ad5aa852b787da0ef`  
		Last Modified: Wed, 11 Dec 2019 22:58:48 GMT  
		Size: 2.2 MB (2229557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b85d9384eb6eca9f83454f40ab447e2eeacfea860348314b3d82ea82238d573`  
		Last Modified: Wed, 11 Dec 2019 22:58:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1545409360129e2ae80d7b8f220f790c5b012b70972f8b64fd0a350483f10c`  
		Last Modified: Wed, 11 Dec 2019 22:59:04 GMT  
		Size: 59.5 MB (59532287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8be6d608ad31e1cc6ef04fd44189715e2bec7defbc9731e56af39548ce97abf`  
		Last Modified: Wed, 11 Dec 2019 22:58:45 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9f1fb9da16c49cce339d24f699837384e3842493dd1a1d48a5904e6d04eebd`  
		Last Modified: Wed, 11 Dec 2019 22:58:45 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107ef206935890f5e3c8d6f7b13c9e231dd9fb87198c07b8b153679d3a07bcd`  
		Last Modified: Wed, 11 Dec 2019 22:58:45 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b770b6bdd361810ea324b9adf28a24ebcbf0bb0520d3b6a4ee53e496bb1ad4`  
		Last Modified: Wed, 11 Dec 2019 22:59:30 GMT  
		Size: 6.6 MB (6593235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8854ae5a4e1458fb0154a525ccc0893a13b9656d54ab27f2d582910a30dcaaf9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70263541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7f16c5d45e9719de4c144047b6384e359e4112fa93e439f12a8a82692e09a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2019 23:39:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 11 Dec 2019 23:39:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 11 Dec 2019 23:39:42 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Dec 2019 23:39:43 GMT
ENV DOCKER_VERSION=19.03.5
# Wed, 11 Dec 2019 23:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Dec 2019 23:39:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Dec 2019 23:39:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Dec 2019 23:39:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Dec 2019 23:39:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Dec 2019 23:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2019 23:39:55 GMT
CMD ["sh"]
# Wed, 11 Dec 2019 23:40:49 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4930edba01571f06733f51438ff75fd189643faaa974ecd081fe02c862f30`  
		Last Modified: Wed, 11 Dec 2019 23:41:12 GMT  
		Size: 2.5 MB (2451440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168cec15ea7d22d62052eca3277505f95f654ea420b93214e439c7bed4e67b95`  
		Last Modified: Wed, 11 Dec 2019 23:41:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b561127bf77d73eae5e1ef05a721ee95b4049642c37de2926df6801485b285e`  
		Last Modified: Wed, 11 Dec 2019 23:41:28 GMT  
		Size: 57.0 MB (57006217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14fc1df435300bb4cc734e1c5ec8835e63a6c4974878ae1df55a0138fbe393`  
		Last Modified: Wed, 11 Dec 2019 23:41:09 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141662ea1213cce657fd7271df8105b45251ae241897b99143f1c4ecae5c4bd1`  
		Last Modified: Wed, 11 Dec 2019 23:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b753173eaf4bfc3b344c536cebf062ddc0d56aa0ab88d30fc4e80cb23e96325`  
		Last Modified: Wed, 11 Dec 2019 23:41:09 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06784639818de54df259278e50245d457fa0bf61002da027f39d8126a8956475`  
		Last Modified: Wed, 11 Dec 2019 23:41:58 GMT  
		Size: 8.1 MB (8086237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
