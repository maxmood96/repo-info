<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5.4`](#kapacitor154)
-	[`kapacitor:1.5.4-alpine`](#kapacitor154-alpine)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:335fa1fc24a2b49354cae3e9aaeed683d937d346dbea9338f24cb3c5daff8ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:fb4dfbf4399867e46ccaebb80f3d5e8c1fce3b229965a7ad939cb0199d62c0ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96305220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b10679e1ef3446ba059c9e182e5ab1ae27f97d5a6eb0a49b1fe07ada41a267`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:45:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 27 Feb 2020 03:45:47 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:45:47 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 27 Feb 2020 03:45:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 27 Feb 2020 03:45:50 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 27 Feb 2020 03:45:50 GMT
EXPOSE 9092
# Thu, 27 Feb 2020 03:45:50 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 27 Feb 2020 03:45:50 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 27 Feb 2020 03:45:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:45:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc43f4da75e578f24047203272c5e96318a3a854bd288fb4b7ec08211bf008`  
		Last Modified: Thu, 27 Feb 2020 03:46:16 GMT  
		Size: 13.1 MB (13094294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ababb2175d176c3f868822a958f4d2e7b03fe0a862768f44c944868b1ce912c`  
		Last Modified: Thu, 27 Feb 2020 03:46:15 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3670641643da0a766b6f6c31f4a3c73c41d46849ac69daf22db7ae421b2590`  
		Last Modified: Thu, 27 Feb 2020 03:46:20 GMT  
		Size: 22.7 MB (22694287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e737225a0514f7f407b60afa35604f046ce3f3c1a5f2886a2a335ea5c8b234`  
		Last Modified: Thu, 27 Feb 2020 03:46:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb2324a6a899053d75b8c4679d46663364eae12824f81c96a546e4f9b78c04d`  
		Last Modified: Thu, 27 Feb 2020 03:46:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:4ca8d73b7acd1174f77c9a235eff99e7f087cdb91fbf90f19002400903bd65e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90092708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8f6e7edeab01e1388714514edada70a35b07b08ab386b6001f3e6092da31e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:33:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 23:33:29 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:33:29 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 31 Mar 2020 23:33:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 23:33:36 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 23:33:37 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 23:33:38 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 23:33:38 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 23:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:33:40 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5432e8ca931a9ca370b212bb819c3bbbfbb9e436742740a68e4f0439b34144c6`  
		Last Modified: Tue, 31 Mar 2020 23:34:14 GMT  
		Size: 13.3 MB (13264207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4d82fc38305c0430392e8f936f8322151333ea52879ea7f27c25647ec5b432`  
		Last Modified: Tue, 31 Mar 2020 23:34:11 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f3f3626007fbc2d3d9352937ad2e68ce4e3f70a4efc1bc090f6bb96cbc65a4`  
		Last Modified: Tue, 31 Mar 2020 23:34:19 GMT  
		Size: 21.3 MB (21308064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82b5d20a60c966a3cc5c9d236f83d3d209e536f78a1026915cc9de6042fca57`  
		Last Modified: Tue, 31 Mar 2020 23:34:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c7ef15afc0c080ec708787412078f20669557fd91ef1dde3daf3860e89db5d`  
		Last Modified: Tue, 31 Mar 2020 23:34:11 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:48c10c32e697f940725207d72da324e3e4ea8d7b3a9c3112dedc686c73c07246
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91113404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3af86319740bed56e29d29da04aa04f6dd3d2d6609fd222172483164bbd8657`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:23:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 21:23:57 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:23:57 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 31 Mar 2020 21:24:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 21:24:04 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 21:24:05 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 21:24:05 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 21:24:06 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 21:24:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:24:07 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d055db7a608faac188175cecb3bee478a8bfc55dbafd64443c8a79359cec76b`  
		Last Modified: Tue, 31 Mar 2020 21:24:36 GMT  
		Size: 12.8 MB (12801310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8de9ed350e7810558076a76d045904f6bac2f625e8e50c357c6c54e0d0b88ce`  
		Last Modified: Tue, 31 Mar 2020 21:24:34 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8017bd8826428d28ce7fdd8aa74147bea890f58341dc706aec6f560a23678de3`  
		Last Modified: Tue, 31 Mar 2020 21:24:42 GMT  
		Size: 21.3 MB (21307863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e9dfa8f903cf0a9fe9aa0dd8aa78c2998a763ee6f58c43d24ce9708f4d0c5`  
		Last Modified: Tue, 31 Mar 2020 21:24:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17263fcfe67d5dad85453d00a67100f9e7cf80d6b06b07edc3070ee3fb2c60be`  
		Last Modified: Tue, 31 Mar 2020 21:24:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:335fa1fc24a2b49354cae3e9aaeed683d937d346dbea9338f24cb3c5daff8ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:fb4dfbf4399867e46ccaebb80f3d5e8c1fce3b229965a7ad939cb0199d62c0ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96305220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b10679e1ef3446ba059c9e182e5ab1ae27f97d5a6eb0a49b1fe07ada41a267`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:45:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 27 Feb 2020 03:45:47 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:45:47 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 27 Feb 2020 03:45:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 27 Feb 2020 03:45:50 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 27 Feb 2020 03:45:50 GMT
EXPOSE 9092
# Thu, 27 Feb 2020 03:45:50 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 27 Feb 2020 03:45:50 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 27 Feb 2020 03:45:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:45:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc43f4da75e578f24047203272c5e96318a3a854bd288fb4b7ec08211bf008`  
		Last Modified: Thu, 27 Feb 2020 03:46:16 GMT  
		Size: 13.1 MB (13094294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ababb2175d176c3f868822a958f4d2e7b03fe0a862768f44c944868b1ce912c`  
		Last Modified: Thu, 27 Feb 2020 03:46:15 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3670641643da0a766b6f6c31f4a3c73c41d46849ac69daf22db7ae421b2590`  
		Last Modified: Thu, 27 Feb 2020 03:46:20 GMT  
		Size: 22.7 MB (22694287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e737225a0514f7f407b60afa35604f046ce3f3c1a5f2886a2a335ea5c8b234`  
		Last Modified: Thu, 27 Feb 2020 03:46:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb2324a6a899053d75b8c4679d46663364eae12824f81c96a546e4f9b78c04d`  
		Last Modified: Thu, 27 Feb 2020 03:46:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:4ca8d73b7acd1174f77c9a235eff99e7f087cdb91fbf90f19002400903bd65e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90092708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8f6e7edeab01e1388714514edada70a35b07b08ab386b6001f3e6092da31e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:33:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 23:33:29 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:33:29 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 31 Mar 2020 23:33:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 23:33:36 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 23:33:37 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 23:33:38 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 23:33:38 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 23:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:33:40 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5432e8ca931a9ca370b212bb819c3bbbfbb9e436742740a68e4f0439b34144c6`  
		Last Modified: Tue, 31 Mar 2020 23:34:14 GMT  
		Size: 13.3 MB (13264207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4d82fc38305c0430392e8f936f8322151333ea52879ea7f27c25647ec5b432`  
		Last Modified: Tue, 31 Mar 2020 23:34:11 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f3f3626007fbc2d3d9352937ad2e68ce4e3f70a4efc1bc090f6bb96cbc65a4`  
		Last Modified: Tue, 31 Mar 2020 23:34:19 GMT  
		Size: 21.3 MB (21308064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82b5d20a60c966a3cc5c9d236f83d3d209e536f78a1026915cc9de6042fca57`  
		Last Modified: Tue, 31 Mar 2020 23:34:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c7ef15afc0c080ec708787412078f20669557fd91ef1dde3daf3860e89db5d`  
		Last Modified: Tue, 31 Mar 2020 23:34:11 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:48c10c32e697f940725207d72da324e3e4ea8d7b3a9c3112dedc686c73c07246
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91113404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3af86319740bed56e29d29da04aa04f6dd3d2d6609fd222172483164bbd8657`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:23:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 21:23:57 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:23:57 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 31 Mar 2020 21:24:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 21:24:04 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 21:24:05 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 21:24:05 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 21:24:06 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 21:24:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:24:07 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d055db7a608faac188175cecb3bee478a8bfc55dbafd64443c8a79359cec76b`  
		Last Modified: Tue, 31 Mar 2020 21:24:36 GMT  
		Size: 12.8 MB (12801310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8de9ed350e7810558076a76d045904f6bac2f625e8e50c357c6c54e0d0b88ce`  
		Last Modified: Tue, 31 Mar 2020 21:24:34 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8017bd8826428d28ce7fdd8aa74147bea890f58341dc706aec6f560a23678de3`  
		Last Modified: Tue, 31 Mar 2020 21:24:42 GMT  
		Size: 21.3 MB (21307863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e9dfa8f903cf0a9fe9aa0dd8aa78c2998a763ee6f58c43d24ce9708f4d0c5`  
		Last Modified: Tue, 31 Mar 2020 21:24:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17263fcfe67d5dad85453d00a67100f9e7cf80d6b06b07edc3070ee3fb2c60be`  
		Last Modified: Tue, 31 Mar 2020 21:24:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:4b7ab5becd898679dbafa450a041ada26f62d51ac2f2d8bd21d849dc028bf159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:6d92d139476006b3b0ccddfab2d4eab3518cd056d479efbe6dc7fd03608e7ffd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19665285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb071dc7f9051052cb755751e2b324785f1b32435fc99257f50dad0c551db5db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:32:40 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 23 Jan 2020 19:32:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:32:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 23 Jan 2020 19:32:47 GMT
EXPOSE 9092
# Thu, 23 Jan 2020 19:32:47 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 23 Jan 2020 19:32:47 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 23 Jan 2020 19:32:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:32:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c407ae7d3cfd95f503dfebe32b93755309be98a50f56e26434bb128be28b25ef`  
		Last Modified: Thu, 23 Jan 2020 19:33:34 GMT  
		Size: 16.6 MB (16598628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59dc41826e7d4d15bccd28b751196d47c47517dc22ca54646217241e0a1cd7`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed2f3fcc2bda9de3b9bbaee5ec5eb2f4198189c69005b51c23e1d951887b638`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:4b7ab5becd898679dbafa450a041ada26f62d51ac2f2d8bd21d849dc028bf159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:6d92d139476006b3b0ccddfab2d4eab3518cd056d479efbe6dc7fd03608e7ffd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19665285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb071dc7f9051052cb755751e2b324785f1b32435fc99257f50dad0c551db5db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:32:40 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 23 Jan 2020 19:32:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:32:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 23 Jan 2020 19:32:47 GMT
EXPOSE 9092
# Thu, 23 Jan 2020 19:32:47 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 23 Jan 2020 19:32:47 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 23 Jan 2020 19:32:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:32:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c407ae7d3cfd95f503dfebe32b93755309be98a50f56e26434bb128be28b25ef`  
		Last Modified: Thu, 23 Jan 2020 19:33:34 GMT  
		Size: 16.6 MB (16598628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59dc41826e7d4d15bccd28b751196d47c47517dc22ca54646217241e0a1cd7`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed2f3fcc2bda9de3b9bbaee5ec5eb2f4198189c69005b51c23e1d951887b638`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:ce85cde2a8d33da7b8071ebef67bccf00106924af7357b7824ae656ade0a3ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:e3db59d4fd3e0412b8971114d7a63bbbbdf8cc53f183387b33b015d5eb13b56b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109921585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59cd84d65697816541763258610a272628b3d9685b6b48f2cdafe671cb72fb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:45:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 27 Feb 2020 03:45:47 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:45:59 GMT
ENV KAPACITOR_VERSION=1.5.4
# Thu, 27 Feb 2020 03:46:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:46:03 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 27 Feb 2020 03:46:03 GMT
EXPOSE 9092
# Thu, 27 Feb 2020 03:46:03 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 27 Feb 2020 03:46:03 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 27 Feb 2020 03:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:46:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc43f4da75e578f24047203272c5e96318a3a854bd288fb4b7ec08211bf008`  
		Last Modified: Thu, 27 Feb 2020 03:46:16 GMT  
		Size: 13.1 MB (13094294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ababb2175d176c3f868822a958f4d2e7b03fe0a862768f44c944868b1ce912c`  
		Last Modified: Thu, 27 Feb 2020 03:46:15 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15557de99a32aa2424540e26625343668366613b85a961ad98a36aecc73d3380`  
		Last Modified: Thu, 27 Feb 2020 03:46:30 GMT  
		Size: 36.3 MB (36310652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5e4e59e69fd4fab3d68f080e2887f875c4e865cfa11a838397871ea13592a3`  
		Last Modified: Thu, 27 Feb 2020 03:46:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a714ff265cd309cedcb8009192fa0e33f9ba860cdc98ac217c1ff2b9bf70cf`  
		Last Modified: Thu, 27 Feb 2020 03:46:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:7980819474e358b9b0bb71cd47fa5a8aafefa345754b5fe2562b4a608a622259
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102833893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea026b1816561fb28a9407c7e0fb96464f3ff02b85e642edad11a7a53f1ad678`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:33:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 23:33:29 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:33:48 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 31 Mar 2020 23:33:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 31 Mar 2020 23:33:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 23:33:57 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 23:33:58 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 23:33:59 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 23:34:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:34:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5432e8ca931a9ca370b212bb819c3bbbfbb9e436742740a68e4f0439b34144c6`  
		Last Modified: Tue, 31 Mar 2020 23:34:14 GMT  
		Size: 13.3 MB (13264207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4d82fc38305c0430392e8f936f8322151333ea52879ea7f27c25647ec5b432`  
		Last Modified: Tue, 31 Mar 2020 23:34:11 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e105520468a2244b998f2198b20cf7589d12b07a788b235f22091df970f3a967`  
		Last Modified: Tue, 31 Mar 2020 23:34:34 GMT  
		Size: 34.0 MB (34049247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12116413a59e56736f40afb82e08a7f633a1b7b3085da6dbb5d1a063e87cfc97`  
		Last Modified: Tue, 31 Mar 2020 23:34:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4392ef227b280d4c527f2947e3200e3decb76b6e6f58bcf0da4d032867f10b8`  
		Last Modified: Tue, 31 Mar 2020 23:34:26 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:b6820483b6a096ea934ad13d0b452870ed328eeb103e9f53eef774dc5c58d490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103854599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acfde5f2284c4577e9af268f3134d6287314d51f06c13935635d19007842fea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:23:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 21:23:57 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:24:13 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 31 Mar 2020 21:24:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 31 Mar 2020 21:24:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 21:24:20 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 21:24:21 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 21:24:21 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 21:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:24:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d055db7a608faac188175cecb3bee478a8bfc55dbafd64443c8a79359cec76b`  
		Last Modified: Tue, 31 Mar 2020 21:24:36 GMT  
		Size: 12.8 MB (12801310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8de9ed350e7810558076a76d045904f6bac2f625e8e50c357c6c54e0d0b88ce`  
		Last Modified: Tue, 31 Mar 2020 21:24:34 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87a5e5af47aa1caca35e13cfbcc113b2848b6539c9fcd4c0bf090472cc6995`  
		Last Modified: Tue, 31 Mar 2020 21:24:59 GMT  
		Size: 34.0 MB (34049058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804cb6eb46360da1b6beb485e39bff9fbdbd64f5df9b405080d6190f0c45cf26`  
		Last Modified: Tue, 31 Mar 2020 21:24:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5211db4561fb0d4e4b7fbc88afd7d589b59063cdd8bb25c3798efcbef3ae1fed`  
		Last Modified: Tue, 31 Mar 2020 21:24:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.4`

```console
$ docker pull kapacitor@sha256:ce85cde2a8d33da7b8071ebef67bccf00106924af7357b7824ae656ade0a3ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:e3db59d4fd3e0412b8971114d7a63bbbbdf8cc53f183387b33b015d5eb13b56b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109921585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59cd84d65697816541763258610a272628b3d9685b6b48f2cdafe671cb72fb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:45:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 27 Feb 2020 03:45:47 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:45:59 GMT
ENV KAPACITOR_VERSION=1.5.4
# Thu, 27 Feb 2020 03:46:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:46:03 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 27 Feb 2020 03:46:03 GMT
EXPOSE 9092
# Thu, 27 Feb 2020 03:46:03 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 27 Feb 2020 03:46:03 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 27 Feb 2020 03:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:46:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc43f4da75e578f24047203272c5e96318a3a854bd288fb4b7ec08211bf008`  
		Last Modified: Thu, 27 Feb 2020 03:46:16 GMT  
		Size: 13.1 MB (13094294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ababb2175d176c3f868822a958f4d2e7b03fe0a862768f44c944868b1ce912c`  
		Last Modified: Thu, 27 Feb 2020 03:46:15 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15557de99a32aa2424540e26625343668366613b85a961ad98a36aecc73d3380`  
		Last Modified: Thu, 27 Feb 2020 03:46:30 GMT  
		Size: 36.3 MB (36310652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5e4e59e69fd4fab3d68f080e2887f875c4e865cfa11a838397871ea13592a3`  
		Last Modified: Thu, 27 Feb 2020 03:46:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a714ff265cd309cedcb8009192fa0e33f9ba860cdc98ac217c1ff2b9bf70cf`  
		Last Modified: Thu, 27 Feb 2020 03:46:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:7980819474e358b9b0bb71cd47fa5a8aafefa345754b5fe2562b4a608a622259
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102833893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea026b1816561fb28a9407c7e0fb96464f3ff02b85e642edad11a7a53f1ad678`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:33:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 23:33:29 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:33:48 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 31 Mar 2020 23:33:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 31 Mar 2020 23:33:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 23:33:57 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 23:33:58 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 23:33:59 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 23:34:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:34:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5432e8ca931a9ca370b212bb819c3bbbfbb9e436742740a68e4f0439b34144c6`  
		Last Modified: Tue, 31 Mar 2020 23:34:14 GMT  
		Size: 13.3 MB (13264207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4d82fc38305c0430392e8f936f8322151333ea52879ea7f27c25647ec5b432`  
		Last Modified: Tue, 31 Mar 2020 23:34:11 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e105520468a2244b998f2198b20cf7589d12b07a788b235f22091df970f3a967`  
		Last Modified: Tue, 31 Mar 2020 23:34:34 GMT  
		Size: 34.0 MB (34049247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12116413a59e56736f40afb82e08a7f633a1b7b3085da6dbb5d1a063e87cfc97`  
		Last Modified: Tue, 31 Mar 2020 23:34:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4392ef227b280d4c527f2947e3200e3decb76b6e6f58bcf0da4d032867f10b8`  
		Last Modified: Tue, 31 Mar 2020 23:34:26 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:b6820483b6a096ea934ad13d0b452870ed328eeb103e9f53eef774dc5c58d490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103854599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acfde5f2284c4577e9af268f3134d6287314d51f06c13935635d19007842fea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:23:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 21:23:57 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:24:13 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 31 Mar 2020 21:24:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 31 Mar 2020 21:24:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 21:24:20 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 21:24:21 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 21:24:21 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 21:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:24:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d055db7a608faac188175cecb3bee478a8bfc55dbafd64443c8a79359cec76b`  
		Last Modified: Tue, 31 Mar 2020 21:24:36 GMT  
		Size: 12.8 MB (12801310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8de9ed350e7810558076a76d045904f6bac2f625e8e50c357c6c54e0d0b88ce`  
		Last Modified: Tue, 31 Mar 2020 21:24:34 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87a5e5af47aa1caca35e13cfbcc113b2848b6539c9fcd4c0bf090472cc6995`  
		Last Modified: Tue, 31 Mar 2020 21:24:59 GMT  
		Size: 34.0 MB (34049058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804cb6eb46360da1b6beb485e39bff9fbdbd64f5df9b405080d6190f0c45cf26`  
		Last Modified: Tue, 31 Mar 2020 21:24:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5211db4561fb0d4e4b7fbc88afd7d589b59063cdd8bb25c3798efcbef3ae1fed`  
		Last Modified: Tue, 31 Mar 2020 21:24:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.4-alpine`

```console
$ docker pull kapacitor@sha256:b41b04ca68ce307ea4df76793be228011d3d492581b4c9b996fcc3cc5369cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:0ec18a89862ad1567d59a589f9a472077188999cd7b788ca3159235b15c65132
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23092042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f81fd4f082beb840496b11d90d70e1307d6e0d14f400ae21e428faf21dc48b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:24:54 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 25 Feb 2020 01:24:58 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:24:58 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 25 Feb 2020 01:24:58 GMT
EXPOSE 9092
# Tue, 25 Feb 2020 01:24:58 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 25 Feb 2020 01:24:59 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Tue, 25 Feb 2020 01:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:24:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3a3a4a913d2075e1dc4f129889b313682e6b193e5be8750a459d162a65bcbe`  
		Last Modified: Tue, 25 Feb 2020 01:25:23 GMT  
		Size: 20.0 MB (20025385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa454331317b4581997009b7b981776670d8eaac40f87132f1a1f56f13e7214a`  
		Last Modified: Tue, 25 Feb 2020 01:25:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581a2bb21bf1b5e5c75b8c19f6ee06cd710ccf81ad10d86edabc900dbfd027e0`  
		Last Modified: Tue, 25 Feb 2020 01:25:18 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:b41b04ca68ce307ea4df76793be228011d3d492581b4c9b996fcc3cc5369cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:0ec18a89862ad1567d59a589f9a472077188999cd7b788ca3159235b15c65132
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23092042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f81fd4f082beb840496b11d90d70e1307d6e0d14f400ae21e428faf21dc48b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:24:54 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 25 Feb 2020 01:24:58 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:24:58 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 25 Feb 2020 01:24:58 GMT
EXPOSE 9092
# Tue, 25 Feb 2020 01:24:58 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 25 Feb 2020 01:24:59 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Tue, 25 Feb 2020 01:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:24:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3a3a4a913d2075e1dc4f129889b313682e6b193e5be8750a459d162a65bcbe`  
		Last Modified: Tue, 25 Feb 2020 01:25:23 GMT  
		Size: 20.0 MB (20025385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa454331317b4581997009b7b981776670d8eaac40f87132f1a1f56f13e7214a`  
		Last Modified: Tue, 25 Feb 2020 01:25:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581a2bb21bf1b5e5c75b8c19f6ee06cd710ccf81ad10d86edabc900dbfd027e0`  
		Last Modified: Tue, 25 Feb 2020 01:25:18 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:b41b04ca68ce307ea4df76793be228011d3d492581b4c9b996fcc3cc5369cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:0ec18a89862ad1567d59a589f9a472077188999cd7b788ca3159235b15c65132
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23092042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f81fd4f082beb840496b11d90d70e1307d6e0d14f400ae21e428faf21dc48b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:24:54 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 25 Feb 2020 01:24:58 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:24:58 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 25 Feb 2020 01:24:58 GMT
EXPOSE 9092
# Tue, 25 Feb 2020 01:24:58 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 25 Feb 2020 01:24:59 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Tue, 25 Feb 2020 01:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:24:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3a3a4a913d2075e1dc4f129889b313682e6b193e5be8750a459d162a65bcbe`  
		Last Modified: Tue, 25 Feb 2020 01:25:23 GMT  
		Size: 20.0 MB (20025385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa454331317b4581997009b7b981776670d8eaac40f87132f1a1f56f13e7214a`  
		Last Modified: Tue, 25 Feb 2020 01:25:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581a2bb21bf1b5e5c75b8c19f6ee06cd710ccf81ad10d86edabc900dbfd027e0`  
		Last Modified: Tue, 25 Feb 2020 01:25:18 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:ce85cde2a8d33da7b8071ebef67bccf00106924af7357b7824ae656ade0a3ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:e3db59d4fd3e0412b8971114d7a63bbbbdf8cc53f183387b33b015d5eb13b56b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109921585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59cd84d65697816541763258610a272628b3d9685b6b48f2cdafe671cb72fb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:45:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 27 Feb 2020 03:45:47 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:45:59 GMT
ENV KAPACITOR_VERSION=1.5.4
# Thu, 27 Feb 2020 03:46:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:46:03 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 27 Feb 2020 03:46:03 GMT
EXPOSE 9092
# Thu, 27 Feb 2020 03:46:03 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 27 Feb 2020 03:46:03 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 27 Feb 2020 03:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:46:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc43f4da75e578f24047203272c5e96318a3a854bd288fb4b7ec08211bf008`  
		Last Modified: Thu, 27 Feb 2020 03:46:16 GMT  
		Size: 13.1 MB (13094294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ababb2175d176c3f868822a958f4d2e7b03fe0a862768f44c944868b1ce912c`  
		Last Modified: Thu, 27 Feb 2020 03:46:15 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15557de99a32aa2424540e26625343668366613b85a961ad98a36aecc73d3380`  
		Last Modified: Thu, 27 Feb 2020 03:46:30 GMT  
		Size: 36.3 MB (36310652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5e4e59e69fd4fab3d68f080e2887f875c4e865cfa11a838397871ea13592a3`  
		Last Modified: Thu, 27 Feb 2020 03:46:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a714ff265cd309cedcb8009192fa0e33f9ba860cdc98ac217c1ff2b9bf70cf`  
		Last Modified: Thu, 27 Feb 2020 03:46:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:7980819474e358b9b0bb71cd47fa5a8aafefa345754b5fe2562b4a608a622259
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102833893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea026b1816561fb28a9407c7e0fb96464f3ff02b85e642edad11a7a53f1ad678`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:33:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 23:33:29 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:33:48 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 31 Mar 2020 23:33:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 31 Mar 2020 23:33:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 23:33:57 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 23:33:58 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 23:33:59 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 23:34:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:34:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5432e8ca931a9ca370b212bb819c3bbbfbb9e436742740a68e4f0439b34144c6`  
		Last Modified: Tue, 31 Mar 2020 23:34:14 GMT  
		Size: 13.3 MB (13264207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4d82fc38305c0430392e8f936f8322151333ea52879ea7f27c25647ec5b432`  
		Last Modified: Tue, 31 Mar 2020 23:34:11 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e105520468a2244b998f2198b20cf7589d12b07a788b235f22091df970f3a967`  
		Last Modified: Tue, 31 Mar 2020 23:34:34 GMT  
		Size: 34.0 MB (34049247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12116413a59e56736f40afb82e08a7f633a1b7b3085da6dbb5d1a063e87cfc97`  
		Last Modified: Tue, 31 Mar 2020 23:34:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4392ef227b280d4c527f2947e3200e3decb76b6e6f58bcf0da4d032867f10b8`  
		Last Modified: Tue, 31 Mar 2020 23:34:26 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:b6820483b6a096ea934ad13d0b452870ed328eeb103e9f53eef774dc5c58d490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103854599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acfde5f2284c4577e9af268f3134d6287314d51f06c13935635d19007842fea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:23:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 31 Mar 2020 21:23:57 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:24:13 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 31 Mar 2020 21:24:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 31 Mar 2020 21:24:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 31 Mar 2020 21:24:20 GMT
EXPOSE 9092
# Tue, 31 Mar 2020 21:24:21 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 31 Mar 2020 21:24:21 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 31 Mar 2020 21:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:24:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d055db7a608faac188175cecb3bee478a8bfc55dbafd64443c8a79359cec76b`  
		Last Modified: Tue, 31 Mar 2020 21:24:36 GMT  
		Size: 12.8 MB (12801310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8de9ed350e7810558076a76d045904f6bac2f625e8e50c357c6c54e0d0b88ce`  
		Last Modified: Tue, 31 Mar 2020 21:24:34 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87a5e5af47aa1caca35e13cfbcc113b2848b6539c9fcd4c0bf090472cc6995`  
		Last Modified: Tue, 31 Mar 2020 21:24:59 GMT  
		Size: 34.0 MB (34049058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804cb6eb46360da1b6beb485e39bff9fbdbd64f5df9b405080d6190f0c45cf26`  
		Last Modified: Tue, 31 Mar 2020 21:24:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5211db4561fb0d4e4b7fbc88afd7d589b59063cdd8bb25c3798efcbef3ae1fed`  
		Last Modified: Tue, 31 Mar 2020 21:24:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
