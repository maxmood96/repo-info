<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:1.5.9`](#kapacitor159)
-	[`kapacitor:1.5.9-alpine`](#kapacitor159-alpine)
-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.1`](#kapacitor161)
-	[`kapacitor:1.6.1-alpine`](#kapacitor161-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:5967cb26eac18f33a2d13c59cb3a0ae850cf754779bcf75bb6b34a0ea1a652d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:7ee5cc55d3775b4fd93d586acdf3dddc8e42f0d4ad9428e039387f776286bebc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111550171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2beacb0c3474099def06dd821420a7a020b98831b23aac28f265ad7d32dfef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Mon, 02 Aug 2021 19:23:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 02 Aug 2021 19:23:54 GMT
ENV KAPACITOR_VERSION=1.5.9
# Mon, 02 Aug 2021 19:23:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 02 Aug 2021 19:23:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:23:59 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:00 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:00 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25fbfb9c13ab0df657641a5d48af23844b2e5471c11060ca9f01ed32ad73821`  
		Last Modified: Mon, 02 Aug 2021 19:24:45 GMT  
		Size: 2.9 KB (2862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3e53c757132b0f502211b074ca188c4d8631d44c0b63c4827f4166ffb02887`  
		Last Modified: Mon, 02 Aug 2021 19:24:50 GMT  
		Size: 37.2 MB (37219390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed75040813652c772392364def52f376667b9c85b259fb9e7fa197fa30cbbe72`  
		Last Modified: Mon, 02 Aug 2021 19:24:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc5dbb1367bc96ab8308ffdb1eec10c0c6303ddd6a033774ccb00a9442056a9`  
		Last Modified: Mon, 02 Aug 2021 19:24:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:fa8774c108c91c9228dfdb4895d77e8156ce7078beacbe5df14e80dd570faa8f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104271842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9286b77e3cbe75f54db402e09788267444987b33209f3544402f4dede4f10f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 02:06:56 GMT
ADD file:544c40297b94c3ecc6561cf7bfef1cdf9763a18ce5e24b6841a1b70d0516d41d in / 
# Thu, 22 Jul 2021 02:06:57 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:22:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 11:00:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Mon, 02 Aug 2021 19:07:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 02 Aug 2021 19:07:04 GMT
ENV KAPACITOR_VERSION=1.5.9
# Mon, 02 Aug 2021 19:07:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 02 Aug 2021 19:07:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:07:15 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:07:15 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:07:16 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 02 Aug 2021 19:07:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:07:17 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b3cc5e47308fe8ded537d7ffdcaba46fcdf803cfe9878bd9264754a50eaa128b`  
		Last Modified: Thu, 22 Jul 2021 02:20:37 GMT  
		Size: 42.1 MB (42120108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf69efd3b547fe4dc472fd34a54c466b82ce51b7f04957779206b5ea0ef9160`  
		Last Modified: Thu, 22 Jul 2021 04:41:23 GMT  
		Size: 10.0 MB (9950872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7430ae4c6b93ca669cc72566a38f952b74dece32c5897c46e51a5907bd5a0c`  
		Last Modified: Thu, 22 Jul 2021 04:41:20 GMT  
		Size: 3.9 MB (3921255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d288a7a9052de99ec8f43901d57a79d2ed295f5365af74abc65676e9d1a597`  
		Last Modified: Fri, 23 Jul 2021 11:01:53 GMT  
		Size: 13.5 MB (13489598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb36f43f4cbd155c5c5a32344bb24914933654ea25e1422e572a1e392906db2`  
		Last Modified: Mon, 02 Aug 2021 19:07:38 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20208ab7a54f03fd8fcae88deeb888eb3c6baba25ef6405f24d6b6c1f7bcaefc`  
		Last Modified: Mon, 02 Aug 2021 19:07:55 GMT  
		Size: 34.8 MB (34786703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc76d6a90f9c20c8b32feb7fd17f0935ff46b5c9af6240f1f1ae363157b99f4`  
		Last Modified: Mon, 02 Aug 2021 19:07:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae6e1cbec3f770e641ddc61f0b846dc9f39a99d4bea489eedabe700511a6cf3`  
		Last Modified: Mon, 02 Aug 2021 19:07:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:68a7b35baa283c4865d5e980280b0276c4d6d14a489f59aea0771babcf3f60d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105079408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b8be3152db041ae15a56f9525aa82925eeeac4e8b4f1e83b6911f9da104c50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:17 GMT
ADD file:79e0d0ec943ec405612e2310514d8f0c72cf83483eea6d5f1a7c28b36fa21cf8 in / 
# Tue, 17 Aug 2021 01:48:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 07:56:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 03:04:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 03:04:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 03:04:32 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 18 Aug 2021 03:04:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 03:04:36 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 03:04:37 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 03:04:37 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 03:04:37 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 03:04:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 03:04:37 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a410f7a7fb8af899e64ef008ec59cc8062766e91abbf21ba5cee65faac7ba3fa`  
		Last Modified: Tue, 17 Aug 2021 01:57:32 GMT  
		Size: 43.2 MB (43177652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e420ab67f91937cc8165f5fb2e94bdab905576eadca5515be250bc6212fe50`  
		Last Modified: Tue, 17 Aug 2021 08:04:49 GMT  
		Size: 10.2 MB (10215748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ce4bbd3804fd1154090db6722050023d8242e910e02ed7d2c09b9795a9d5ac`  
		Last Modified: Tue, 17 Aug 2021 08:04:48 GMT  
		Size: 4.1 MB (4096582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ac1cfab8790dc49973599fa396ed1be6d7c7941973b59135f515444b730be`  
		Last Modified: Wed, 18 Aug 2021 03:05:10 GMT  
		Size: 13.0 MB (13025171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918b8c0940b453d44ba7db5d3637f4123eb859a3817e86d547b0a677ec9bb051`  
		Last Modified: Wed, 18 Aug 2021 03:05:08 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39479fb4a2cddd3ed9efab594360312005a73c1cda58b6f94d8480b9a4a80cdf`  
		Last Modified: Wed, 18 Aug 2021 03:05:13 GMT  
		Size: 34.6 MB (34560947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b292b729814b071d5e0c0a7f4a22bdfb6f81a76482c197a075352b364cbeb66`  
		Last Modified: Wed, 18 Aug 2021 03:05:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe27079a3de6524ec3c861601187a9acb6ebf2e7a9b0802eb1ab1215628444a`  
		Last Modified: Wed, 18 Aug 2021 03:05:08 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:b2ccc7afa0b1ad90265e1e51b967fea685ba85abe2faaa7458d4ce3dac7be39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:eb1a17b8bc033d2344020d564600cf6a69b3e3297b359abcb0016ed619feabc6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22624118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001840f1027f249f88b93c2f7d98dbd027dda8c5cd27ba937ab9ac3f73735b49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 23:05:40 GMT
ENV KAPACITOR_VERSION=1.5.9
# Mon, 02 Aug 2021 19:24:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 02 Aug 2021 19:24:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:24:09 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:09 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:09 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3529096fc7081df43f8950a74b77ba719f8865fbf0fd4ff92e9a5db3ac5a51`  
		Last Modified: Mon, 02 Aug 2021 19:25:05 GMT  
		Size: 19.5 MB (19542043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31170b29ca7609fca0dd052afef629300ba3902dd9829a89c5841dd8cac37f13`  
		Last Modified: Mon, 02 Aug 2021 19:25:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92602239c42b86e0df30d2d05cd5029f676d22bf362de30c1422848a1b2a914`  
		Last Modified: Mon, 02 Aug 2021 19:25:01 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9`

```console
$ docker pull kapacitor@sha256:5967cb26eac18f33a2d13c59cb3a0ae850cf754779bcf75bb6b34a0ea1a652d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.9` - linux; amd64

```console
$ docker pull kapacitor@sha256:7ee5cc55d3775b4fd93d586acdf3dddc8e42f0d4ad9428e039387f776286bebc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111550171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2beacb0c3474099def06dd821420a7a020b98831b23aac28f265ad7d32dfef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Mon, 02 Aug 2021 19:23:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 02 Aug 2021 19:23:54 GMT
ENV KAPACITOR_VERSION=1.5.9
# Mon, 02 Aug 2021 19:23:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 02 Aug 2021 19:23:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:23:59 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:00 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:00 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25fbfb9c13ab0df657641a5d48af23844b2e5471c11060ca9f01ed32ad73821`  
		Last Modified: Mon, 02 Aug 2021 19:24:45 GMT  
		Size: 2.9 KB (2862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3e53c757132b0f502211b074ca188c4d8631d44c0b63c4827f4166ffb02887`  
		Last Modified: Mon, 02 Aug 2021 19:24:50 GMT  
		Size: 37.2 MB (37219390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed75040813652c772392364def52f376667b9c85b259fb9e7fa197fa30cbbe72`  
		Last Modified: Mon, 02 Aug 2021 19:24:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc5dbb1367bc96ab8308ffdb1eec10c0c6303ddd6a033774ccb00a9442056a9`  
		Last Modified: Mon, 02 Aug 2021 19:24:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:fa8774c108c91c9228dfdb4895d77e8156ce7078beacbe5df14e80dd570faa8f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104271842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9286b77e3cbe75f54db402e09788267444987b33209f3544402f4dede4f10f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 02:06:56 GMT
ADD file:544c40297b94c3ecc6561cf7bfef1cdf9763a18ce5e24b6841a1b70d0516d41d in / 
# Thu, 22 Jul 2021 02:06:57 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:22:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 11:00:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Mon, 02 Aug 2021 19:07:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 02 Aug 2021 19:07:04 GMT
ENV KAPACITOR_VERSION=1.5.9
# Mon, 02 Aug 2021 19:07:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 02 Aug 2021 19:07:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:07:15 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:07:15 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:07:16 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 02 Aug 2021 19:07:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:07:17 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b3cc5e47308fe8ded537d7ffdcaba46fcdf803cfe9878bd9264754a50eaa128b`  
		Last Modified: Thu, 22 Jul 2021 02:20:37 GMT  
		Size: 42.1 MB (42120108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf69efd3b547fe4dc472fd34a54c466b82ce51b7f04957779206b5ea0ef9160`  
		Last Modified: Thu, 22 Jul 2021 04:41:23 GMT  
		Size: 10.0 MB (9950872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7430ae4c6b93ca669cc72566a38f952b74dece32c5897c46e51a5907bd5a0c`  
		Last Modified: Thu, 22 Jul 2021 04:41:20 GMT  
		Size: 3.9 MB (3921255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d288a7a9052de99ec8f43901d57a79d2ed295f5365af74abc65676e9d1a597`  
		Last Modified: Fri, 23 Jul 2021 11:01:53 GMT  
		Size: 13.5 MB (13489598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb36f43f4cbd155c5c5a32344bb24914933654ea25e1422e572a1e392906db2`  
		Last Modified: Mon, 02 Aug 2021 19:07:38 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20208ab7a54f03fd8fcae88deeb888eb3c6baba25ef6405f24d6b6c1f7bcaefc`  
		Last Modified: Mon, 02 Aug 2021 19:07:55 GMT  
		Size: 34.8 MB (34786703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc76d6a90f9c20c8b32feb7fd17f0935ff46b5c9af6240f1f1ae363157b99f4`  
		Last Modified: Mon, 02 Aug 2021 19:07:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae6e1cbec3f770e641ddc61f0b846dc9f39a99d4bea489eedabe700511a6cf3`  
		Last Modified: Mon, 02 Aug 2021 19:07:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:68a7b35baa283c4865d5e980280b0276c4d6d14a489f59aea0771babcf3f60d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105079408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b8be3152db041ae15a56f9525aa82925eeeac4e8b4f1e83b6911f9da104c50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:17 GMT
ADD file:79e0d0ec943ec405612e2310514d8f0c72cf83483eea6d5f1a7c28b36fa21cf8 in / 
# Tue, 17 Aug 2021 01:48:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 07:56:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 03:04:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 03:04:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 03:04:32 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 18 Aug 2021 03:04:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 03:04:36 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 03:04:37 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 03:04:37 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 03:04:37 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 03:04:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 03:04:37 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a410f7a7fb8af899e64ef008ec59cc8062766e91abbf21ba5cee65faac7ba3fa`  
		Last Modified: Tue, 17 Aug 2021 01:57:32 GMT  
		Size: 43.2 MB (43177652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e420ab67f91937cc8165f5fb2e94bdab905576eadca5515be250bc6212fe50`  
		Last Modified: Tue, 17 Aug 2021 08:04:49 GMT  
		Size: 10.2 MB (10215748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ce4bbd3804fd1154090db6722050023d8242e910e02ed7d2c09b9795a9d5ac`  
		Last Modified: Tue, 17 Aug 2021 08:04:48 GMT  
		Size: 4.1 MB (4096582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ac1cfab8790dc49973599fa396ed1be6d7c7941973b59135f515444b730be`  
		Last Modified: Wed, 18 Aug 2021 03:05:10 GMT  
		Size: 13.0 MB (13025171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918b8c0940b453d44ba7db5d3637f4123eb859a3817e86d547b0a677ec9bb051`  
		Last Modified: Wed, 18 Aug 2021 03:05:08 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39479fb4a2cddd3ed9efab594360312005a73c1cda58b6f94d8480b9a4a80cdf`  
		Last Modified: Wed, 18 Aug 2021 03:05:13 GMT  
		Size: 34.6 MB (34560947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b292b729814b071d5e0c0a7f4a22bdfb6f81a76482c197a075352b364cbeb66`  
		Last Modified: Wed, 18 Aug 2021 03:05:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe27079a3de6524ec3c861601187a9acb6ebf2e7a9b0802eb1ab1215628444a`  
		Last Modified: Wed, 18 Aug 2021 03:05:08 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9-alpine`

```console
$ docker pull kapacitor@sha256:b2ccc7afa0b1ad90265e1e51b967fea685ba85abe2faaa7458d4ce3dac7be39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5.9-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:eb1a17b8bc033d2344020d564600cf6a69b3e3297b359abcb0016ed619feabc6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22624118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001840f1027f249f88b93c2f7d98dbd027dda8c5cd27ba937ab9ac3f73735b49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 23:05:40 GMT
ENV KAPACITOR_VERSION=1.5.9
# Mon, 02 Aug 2021 19:24:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 02 Aug 2021 19:24:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:24:09 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:09 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:09 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3529096fc7081df43f8950a74b77ba719f8865fbf0fd4ff92e9a5db3ac5a51`  
		Last Modified: Mon, 02 Aug 2021 19:25:05 GMT  
		Size: 19.5 MB (19542043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31170b29ca7609fca0dd052afef629300ba3902dd9829a89c5841dd8cac37f13`  
		Last Modified: Mon, 02 Aug 2021 19:25:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92602239c42b86e0df30d2d05cd5029f676d22bf362de30c1422848a1b2a914`  
		Last Modified: Mon, 02 Aug 2021 19:25:01 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:c6f17cef10a612a8146866434ec4a2ab31f14ed8480f5cb89f720153b61dc46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:f7cfa6bdc09609540420b436d4ccd3eb01edcd6a22910a02713ad73f52c5f64b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133592913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665686f36921dc2ab484d12ae00edbec04ef5a63bbbdec3db092318e54914f60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Mon, 02 Aug 2021 19:23:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 02 Aug 2021 19:24:13 GMT
ENV KAPACITOR_VERSION=1.6.1
# Mon, 02 Aug 2021 19:24:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 02 Aug 2021 19:24:17 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:24:17 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:18 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:18 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:18 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25fbfb9c13ab0df657641a5d48af23844b2e5471c11060ca9f01ed32ad73821`  
		Last Modified: Mon, 02 Aug 2021 19:24:45 GMT  
		Size: 2.9 KB (2862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178da08a09e78306ff155bc95eb9f7966e04b206ad5ee2b2ef95c554ca8051f`  
		Last Modified: Mon, 02 Aug 2021 19:25:23 GMT  
		Size: 59.3 MB (59262132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497922162e899a0d845861c65a7508d496278e7a419a3ff3de8418197abb2c01`  
		Last Modified: Mon, 02 Aug 2021 19:25:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d7f7f11900865847ee71ae8afd452d3406cd5bca82125dc34b314b3c46d8a6`  
		Last Modified: Mon, 02 Aug 2021 19:25:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:bb3c234e66dfa59d248b87cee4296683b657746d08d662675aa83d300aaf5957
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126412617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2d82c3b2c970a55952ec9459906b48548ebfe5e31952e7027918bc433967e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:17 GMT
ADD file:79e0d0ec943ec405612e2310514d8f0c72cf83483eea6d5f1a7c28b36fa21cf8 in / 
# Tue, 17 Aug 2021 01:48:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 07:56:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 03:04:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 03:04:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 03:04:43 GMT
ENV KAPACITOR_VERSION=1.6.1
# Wed, 18 Aug 2021 03:04:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 03:04:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 03:04:47 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 03:04:48 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 03:04:48 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 03:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 03:04:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a410f7a7fb8af899e64ef008ec59cc8062766e91abbf21ba5cee65faac7ba3fa`  
		Last Modified: Tue, 17 Aug 2021 01:57:32 GMT  
		Size: 43.2 MB (43177652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e420ab67f91937cc8165f5fb2e94bdab905576eadca5515be250bc6212fe50`  
		Last Modified: Tue, 17 Aug 2021 08:04:49 GMT  
		Size: 10.2 MB (10215748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ce4bbd3804fd1154090db6722050023d8242e910e02ed7d2c09b9795a9d5ac`  
		Last Modified: Tue, 17 Aug 2021 08:04:48 GMT  
		Size: 4.1 MB (4096582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ac1cfab8790dc49973599fa396ed1be6d7c7941973b59135f515444b730be`  
		Last Modified: Wed, 18 Aug 2021 03:05:10 GMT  
		Size: 13.0 MB (13025171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918b8c0940b453d44ba7db5d3637f4123eb859a3817e86d547b0a677ec9bb051`  
		Last Modified: Wed, 18 Aug 2021 03:05:08 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b545f7a05e164a6464596480ab593368549e63552f2c253130589d7a69dffa3`  
		Last Modified: Wed, 18 Aug 2021 03:05:33 GMT  
		Size: 55.9 MB (55894157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22483778e68af06d02517e68ca78f872bcdd3558272fe774717854d2e191693`  
		Last Modified: Wed, 18 Aug 2021 03:05:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98f8758a8b6b71214bc116749a3a506c46efa2a44a7655f0cc6e97aef2c9221`  
		Last Modified: Wed, 18 Aug 2021 03:05:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:f17e0db5660f63f3446dc74c8c809851bc596a914f8fde21146ab42bed4d9031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c747c3309b95ca8f989738fa859ed28a80e4fd8379fc8545b2862abb43794a78
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62281683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c69dcdbf8b229cee2ca8a5925a542d20c10dfbed63ba270e61c0c6521928fcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 02 Aug 2021 19:24:21 GMT
ENV KAPACITOR_VERSION=1.6.1
# Mon, 02 Aug 2021 19:24:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 02 Aug 2021 19:24:28 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:24:28 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:28 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:28 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cf4b08eddd0084d298e116e9355530da47f17fdfe7c8cc7f753169d8466a2a`  
		Last Modified: Mon, 02 Aug 2021 19:25:44 GMT  
		Size: 59.2 MB (59199609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d9ac724e6a6c56ea83b28de104134c31749e4bf41606568eec6380a3f05917`  
		Last Modified: Mon, 02 Aug 2021 19:25:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12fa3366972ee0c0110a9f9a075ff4299cb66c775ad820dc0e81c1ae12c42f`  
		Last Modified: Mon, 02 Aug 2021 19:25:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.1`

```console
$ docker pull kapacitor@sha256:c6f17cef10a612a8146866434ec4a2ab31f14ed8480f5cb89f720153b61dc46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:f7cfa6bdc09609540420b436d4ccd3eb01edcd6a22910a02713ad73f52c5f64b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133592913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665686f36921dc2ab484d12ae00edbec04ef5a63bbbdec3db092318e54914f60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Mon, 02 Aug 2021 19:23:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 02 Aug 2021 19:24:13 GMT
ENV KAPACITOR_VERSION=1.6.1
# Mon, 02 Aug 2021 19:24:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 02 Aug 2021 19:24:17 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:24:17 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:18 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:18 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:18 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25fbfb9c13ab0df657641a5d48af23844b2e5471c11060ca9f01ed32ad73821`  
		Last Modified: Mon, 02 Aug 2021 19:24:45 GMT  
		Size: 2.9 KB (2862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178da08a09e78306ff155bc95eb9f7966e04b206ad5ee2b2ef95c554ca8051f`  
		Last Modified: Mon, 02 Aug 2021 19:25:23 GMT  
		Size: 59.3 MB (59262132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497922162e899a0d845861c65a7508d496278e7a419a3ff3de8418197abb2c01`  
		Last Modified: Mon, 02 Aug 2021 19:25:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d7f7f11900865847ee71ae8afd452d3406cd5bca82125dc34b314b3c46d8a6`  
		Last Modified: Mon, 02 Aug 2021 19:25:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:bb3c234e66dfa59d248b87cee4296683b657746d08d662675aa83d300aaf5957
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126412617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2d82c3b2c970a55952ec9459906b48548ebfe5e31952e7027918bc433967e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:17 GMT
ADD file:79e0d0ec943ec405612e2310514d8f0c72cf83483eea6d5f1a7c28b36fa21cf8 in / 
# Tue, 17 Aug 2021 01:48:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 07:56:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 03:04:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 03:04:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 03:04:43 GMT
ENV KAPACITOR_VERSION=1.6.1
# Wed, 18 Aug 2021 03:04:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 03:04:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 03:04:47 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 03:04:48 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 03:04:48 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 03:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 03:04:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a410f7a7fb8af899e64ef008ec59cc8062766e91abbf21ba5cee65faac7ba3fa`  
		Last Modified: Tue, 17 Aug 2021 01:57:32 GMT  
		Size: 43.2 MB (43177652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e420ab67f91937cc8165f5fb2e94bdab905576eadca5515be250bc6212fe50`  
		Last Modified: Tue, 17 Aug 2021 08:04:49 GMT  
		Size: 10.2 MB (10215748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ce4bbd3804fd1154090db6722050023d8242e910e02ed7d2c09b9795a9d5ac`  
		Last Modified: Tue, 17 Aug 2021 08:04:48 GMT  
		Size: 4.1 MB (4096582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ac1cfab8790dc49973599fa396ed1be6d7c7941973b59135f515444b730be`  
		Last Modified: Wed, 18 Aug 2021 03:05:10 GMT  
		Size: 13.0 MB (13025171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918b8c0940b453d44ba7db5d3637f4123eb859a3817e86d547b0a677ec9bb051`  
		Last Modified: Wed, 18 Aug 2021 03:05:08 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b545f7a05e164a6464596480ab593368549e63552f2c253130589d7a69dffa3`  
		Last Modified: Wed, 18 Aug 2021 03:05:33 GMT  
		Size: 55.9 MB (55894157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22483778e68af06d02517e68ca78f872bcdd3558272fe774717854d2e191693`  
		Last Modified: Wed, 18 Aug 2021 03:05:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98f8758a8b6b71214bc116749a3a506c46efa2a44a7655f0cc6e97aef2c9221`  
		Last Modified: Wed, 18 Aug 2021 03:05:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.1-alpine`

```console
$ docker pull kapacitor@sha256:f17e0db5660f63f3446dc74c8c809851bc596a914f8fde21146ab42bed4d9031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c747c3309b95ca8f989738fa859ed28a80e4fd8379fc8545b2862abb43794a78
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62281683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c69dcdbf8b229cee2ca8a5925a542d20c10dfbed63ba270e61c0c6521928fcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 02 Aug 2021 19:24:21 GMT
ENV KAPACITOR_VERSION=1.6.1
# Mon, 02 Aug 2021 19:24:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 02 Aug 2021 19:24:28 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:24:28 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:28 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:28 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cf4b08eddd0084d298e116e9355530da47f17fdfe7c8cc7f753169d8466a2a`  
		Last Modified: Mon, 02 Aug 2021 19:25:44 GMT  
		Size: 59.2 MB (59199609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d9ac724e6a6c56ea83b28de104134c31749e4bf41606568eec6380a3f05917`  
		Last Modified: Mon, 02 Aug 2021 19:25:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12fa3366972ee0c0110a9f9a075ff4299cb66c775ad820dc0e81c1ae12c42f`  
		Last Modified: Mon, 02 Aug 2021 19:25:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:f17e0db5660f63f3446dc74c8c809851bc596a914f8fde21146ab42bed4d9031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c747c3309b95ca8f989738fa859ed28a80e4fd8379fc8545b2862abb43794a78
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62281683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c69dcdbf8b229cee2ca8a5925a542d20c10dfbed63ba270e61c0c6521928fcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 02 Aug 2021 19:24:21 GMT
ENV KAPACITOR_VERSION=1.6.1
# Mon, 02 Aug 2021 19:24:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 02 Aug 2021 19:24:28 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:24:28 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:28 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:28 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cf4b08eddd0084d298e116e9355530da47f17fdfe7c8cc7f753169d8466a2a`  
		Last Modified: Mon, 02 Aug 2021 19:25:44 GMT  
		Size: 59.2 MB (59199609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d9ac724e6a6c56ea83b28de104134c31749e4bf41606568eec6380a3f05917`  
		Last Modified: Mon, 02 Aug 2021 19:25:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12fa3366972ee0c0110a9f9a075ff4299cb66c775ad820dc0e81c1ae12c42f`  
		Last Modified: Mon, 02 Aug 2021 19:25:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:c6f17cef10a612a8146866434ec4a2ab31f14ed8480f5cb89f720153b61dc46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:f7cfa6bdc09609540420b436d4ccd3eb01edcd6a22910a02713ad73f52c5f64b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133592913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665686f36921dc2ab484d12ae00edbec04ef5a63bbbdec3db092318e54914f60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Mon, 02 Aug 2021 19:23:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 02 Aug 2021 19:24:13 GMT
ENV KAPACITOR_VERSION=1.6.1
# Mon, 02 Aug 2021 19:24:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 02 Aug 2021 19:24:17 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 02 Aug 2021 19:24:17 GMT
EXPOSE 9092
# Mon, 02 Aug 2021 19:24:18 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 02 Aug 2021 19:24:18 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 02 Aug 2021 19:24:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Aug 2021 19:24:18 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25fbfb9c13ab0df657641a5d48af23844b2e5471c11060ca9f01ed32ad73821`  
		Last Modified: Mon, 02 Aug 2021 19:24:45 GMT  
		Size: 2.9 KB (2862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178da08a09e78306ff155bc95eb9f7966e04b206ad5ee2b2ef95c554ca8051f`  
		Last Modified: Mon, 02 Aug 2021 19:25:23 GMT  
		Size: 59.3 MB (59262132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497922162e899a0d845861c65a7508d496278e7a419a3ff3de8418197abb2c01`  
		Last Modified: Mon, 02 Aug 2021 19:25:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d7f7f11900865847ee71ae8afd452d3406cd5bca82125dc34b314b3c46d8a6`  
		Last Modified: Mon, 02 Aug 2021 19:25:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:bb3c234e66dfa59d248b87cee4296683b657746d08d662675aa83d300aaf5957
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126412617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2d82c3b2c970a55952ec9459906b48548ebfe5e31952e7027918bc433967e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:17 GMT
ADD file:79e0d0ec943ec405612e2310514d8f0c72cf83483eea6d5f1a7c28b36fa21cf8 in / 
# Tue, 17 Aug 2021 01:48:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 07:56:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 03:04:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 03:04:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 03:04:43 GMT
ENV KAPACITOR_VERSION=1.6.1
# Wed, 18 Aug 2021 03:04:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 03:04:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 03:04:47 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 03:04:48 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 03:04:48 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 03:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 03:04:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a410f7a7fb8af899e64ef008ec59cc8062766e91abbf21ba5cee65faac7ba3fa`  
		Last Modified: Tue, 17 Aug 2021 01:57:32 GMT  
		Size: 43.2 MB (43177652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e420ab67f91937cc8165f5fb2e94bdab905576eadca5515be250bc6212fe50`  
		Last Modified: Tue, 17 Aug 2021 08:04:49 GMT  
		Size: 10.2 MB (10215748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ce4bbd3804fd1154090db6722050023d8242e910e02ed7d2c09b9795a9d5ac`  
		Last Modified: Tue, 17 Aug 2021 08:04:48 GMT  
		Size: 4.1 MB (4096582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ac1cfab8790dc49973599fa396ed1be6d7c7941973b59135f515444b730be`  
		Last Modified: Wed, 18 Aug 2021 03:05:10 GMT  
		Size: 13.0 MB (13025171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918b8c0940b453d44ba7db5d3637f4123eb859a3817e86d547b0a677ec9bb051`  
		Last Modified: Wed, 18 Aug 2021 03:05:08 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b545f7a05e164a6464596480ab593368549e63552f2c253130589d7a69dffa3`  
		Last Modified: Wed, 18 Aug 2021 03:05:33 GMT  
		Size: 55.9 MB (55894157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22483778e68af06d02517e68ca78f872bcdd3558272fe774717854d2e191693`  
		Last Modified: Wed, 18 Aug 2021 03:05:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98f8758a8b6b71214bc116749a3a506c46efa2a44a7655f0cc6e97aef2c9221`  
		Last Modified: Wed, 18 Aug 2021 03:05:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
