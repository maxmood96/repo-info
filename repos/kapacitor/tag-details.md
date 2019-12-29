<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5.3`](#kapacitor153)
-	[`kapacitor:1.5.3-alpine`](#kapacitor153-alpine)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:7017d8eaec088b7eb6efffb449477da6bc99d02b1599a9d6ed41eea11c49953f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:e3f672816666930f7ef94006713545a02722d7b9d9172d68a1b7af67a708a5ac
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96302319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f44c2e87fd349367eecaf24de10bf8c6e4a27a4d997240848ef04277e973f70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:26:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 06:26:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:26:15 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sun, 29 Dec 2019 06:26:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:26:19 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 06:26:19 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 06:26:19 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 06:26:19 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 06:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:26:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54eac68a8c25638e1bfd43b2780191c95eda5f66706d58161f9c254283bbc12`  
		Last Modified: Sun, 29 Dec 2019 06:26:45 GMT  
		Size: 13.1 MB (13086759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ea20cbb970f30a2c63fcaa1eb4ad0c4ca4f87be733a557ad2d068cfdab808`  
		Last Modified: Sun, 29 Dec 2019 06:26:44 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561ce68aadeb48bf1a1f28a292b4e44cb2583368127b94fe33c4771c8feb6c9a`  
		Last Modified: Sun, 29 Dec 2019 06:26:51 GMT  
		Size: 22.7 MB (22694250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b11aff4704cc6560ce279ecf18c93814ea56f1b101552dcb581a54cbc2a56a0`  
		Last Modified: Sun, 29 Dec 2019 06:26:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6879f5bed3fc55bbb556662de43470402cfb0d74e24800ae4faff44c40e5dc37`  
		Last Modified: Sun, 29 Dec 2019 06:26:44 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:c658681c3b4176f5f46840840e379ac00e35c33be72a9f152aab4bebd9612dee
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90092818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec461049d1b8b4742c30279cce6be39a15d3a0e50500937f3966fea802a4d334`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:34:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 28 Dec 2019 22:34:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:34:23 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 28 Dec 2019 22:34:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:34:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 28 Dec 2019 22:34:31 GMT
EXPOSE 9092
# Sat, 28 Dec 2019 22:34:32 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 28 Dec 2019 22:34:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 28 Dec 2019 22:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:34:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0884195a19c3699ef8c01d1729c1d3961aab5516da4e144c15a158dbeefa18f4`  
		Last Modified: Sat, 28 Dec 2019 22:35:12 GMT  
		Size: 13.3 MB (13256456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e60aaff33912d1472d4b2aea78d7892382813574a8d54017328194c24f19f0d`  
		Last Modified: Sat, 28 Dec 2019 22:35:10 GMT  
		Size: 2.8 KB (2807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c6be8b8a8c5017e3f005c1e2fa2b521c380b4505677702f6d9b6dfe152b9f7`  
		Last Modified: Sat, 28 Dec 2019 22:35:19 GMT  
		Size: 21.3 MB (21308050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6908936737ba3e4806b9f9aa566f7678d20bfd23b39ed40b4a7e2b9a11996513`  
		Last Modified: Sat, 28 Dec 2019 22:35:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be2a97929793b040ad28f7a672dfd81c21281b438e81e1316977cacb66d7129`  
		Last Modified: Sat, 28 Dec 2019 22:35:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:54b9b543af08cdda4d4383cfe5fda2c5d7f834e2db417747ab3bb8c5f678e5d2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91114763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad895eeac045258ab73bf007e44dd7e985f26f6143e4332d8ba597f8c95e811e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:15:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 00:32:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 00:32:44 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 00:32:47 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sun, 29 Dec 2019 00:33:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 00:33:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 00:33:18 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 00:33:21 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 00:33:25 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 00:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 00:33:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f31062581dadb1f69c43e9441040dd46788bf13ae51f20c66929fac82b506b`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 9.7 MB (9748258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62337a296a607f48a5dc3a7c07639360d98e0e78982ca8e459c832719012f12`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 4.1 MB (4094448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58545439b4e40db5dab6e07f70e26ad455d4de4843cb02c2f7f2aa6305b9a626`  
		Last Modified: Sun, 29 Dec 2019 00:34:16 GMT  
		Size: 12.8 MB (12794461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6bfca4f9e2f8f017e83cf18a76193e51f5c4714e487d978f5e508416626293`  
		Last Modified: Sun, 29 Dec 2019 00:34:14 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b4961f70f4fe37e5070bf11822c27496ae44d6c79c7eda1060792c7f98680a`  
		Last Modified: Sun, 29 Dec 2019 00:34:21 GMT  
		Size: 21.3 MB (21307861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef1084b5f31b2bbfcb89cafda1fac70909c4cc6f4b2179bc43a3a76eeb27f5`  
		Last Modified: Sun, 29 Dec 2019 00:34:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb9b74d76f9e9e0e4f9deb7cf9193b12eee0117e7feb2b2a4aba35962c68b60`  
		Last Modified: Sun, 29 Dec 2019 00:34:14 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:7017d8eaec088b7eb6efffb449477da6bc99d02b1599a9d6ed41eea11c49953f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:e3f672816666930f7ef94006713545a02722d7b9d9172d68a1b7af67a708a5ac
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96302319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f44c2e87fd349367eecaf24de10bf8c6e4a27a4d997240848ef04277e973f70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:26:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 06:26:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:26:15 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sun, 29 Dec 2019 06:26:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:26:19 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 06:26:19 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 06:26:19 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 06:26:19 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 06:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:26:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54eac68a8c25638e1bfd43b2780191c95eda5f66706d58161f9c254283bbc12`  
		Last Modified: Sun, 29 Dec 2019 06:26:45 GMT  
		Size: 13.1 MB (13086759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ea20cbb970f30a2c63fcaa1eb4ad0c4ca4f87be733a557ad2d068cfdab808`  
		Last Modified: Sun, 29 Dec 2019 06:26:44 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561ce68aadeb48bf1a1f28a292b4e44cb2583368127b94fe33c4771c8feb6c9a`  
		Last Modified: Sun, 29 Dec 2019 06:26:51 GMT  
		Size: 22.7 MB (22694250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b11aff4704cc6560ce279ecf18c93814ea56f1b101552dcb581a54cbc2a56a0`  
		Last Modified: Sun, 29 Dec 2019 06:26:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6879f5bed3fc55bbb556662de43470402cfb0d74e24800ae4faff44c40e5dc37`  
		Last Modified: Sun, 29 Dec 2019 06:26:44 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:c658681c3b4176f5f46840840e379ac00e35c33be72a9f152aab4bebd9612dee
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90092818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec461049d1b8b4742c30279cce6be39a15d3a0e50500937f3966fea802a4d334`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:34:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 28 Dec 2019 22:34:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:34:23 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 28 Dec 2019 22:34:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:34:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 28 Dec 2019 22:34:31 GMT
EXPOSE 9092
# Sat, 28 Dec 2019 22:34:32 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 28 Dec 2019 22:34:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 28 Dec 2019 22:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:34:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0884195a19c3699ef8c01d1729c1d3961aab5516da4e144c15a158dbeefa18f4`  
		Last Modified: Sat, 28 Dec 2019 22:35:12 GMT  
		Size: 13.3 MB (13256456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e60aaff33912d1472d4b2aea78d7892382813574a8d54017328194c24f19f0d`  
		Last Modified: Sat, 28 Dec 2019 22:35:10 GMT  
		Size: 2.8 KB (2807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c6be8b8a8c5017e3f005c1e2fa2b521c380b4505677702f6d9b6dfe152b9f7`  
		Last Modified: Sat, 28 Dec 2019 22:35:19 GMT  
		Size: 21.3 MB (21308050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6908936737ba3e4806b9f9aa566f7678d20bfd23b39ed40b4a7e2b9a11996513`  
		Last Modified: Sat, 28 Dec 2019 22:35:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be2a97929793b040ad28f7a672dfd81c21281b438e81e1316977cacb66d7129`  
		Last Modified: Sat, 28 Dec 2019 22:35:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:54b9b543af08cdda4d4383cfe5fda2c5d7f834e2db417747ab3bb8c5f678e5d2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91114763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad895eeac045258ab73bf007e44dd7e985f26f6143e4332d8ba597f8c95e811e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:15:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 00:32:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 00:32:44 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 00:32:47 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sun, 29 Dec 2019 00:33:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 00:33:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 00:33:18 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 00:33:21 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 00:33:25 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 00:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 00:33:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f31062581dadb1f69c43e9441040dd46788bf13ae51f20c66929fac82b506b`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 9.7 MB (9748258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62337a296a607f48a5dc3a7c07639360d98e0e78982ca8e459c832719012f12`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 4.1 MB (4094448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58545439b4e40db5dab6e07f70e26ad455d4de4843cb02c2f7f2aa6305b9a626`  
		Last Modified: Sun, 29 Dec 2019 00:34:16 GMT  
		Size: 12.8 MB (12794461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6bfca4f9e2f8f017e83cf18a76193e51f5c4714e487d978f5e508416626293`  
		Last Modified: Sun, 29 Dec 2019 00:34:14 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b4961f70f4fe37e5070bf11822c27496ae44d6c79c7eda1060792c7f98680a`  
		Last Modified: Sun, 29 Dec 2019 00:34:21 GMT  
		Size: 21.3 MB (21307861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef1084b5f31b2bbfcb89cafda1fac70909c4cc6f4b2179bc43a3a76eeb27f5`  
		Last Modified: Sun, 29 Dec 2019 00:34:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb9b74d76f9e9e0e4f9deb7cf9193b12eee0117e7feb2b2a4aba35962c68b60`  
		Last Modified: Sun, 29 Dec 2019 00:34:14 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:5b377752983e68e39b3bf0b7b54f6e939f3e4cd74a186cdd3ce3fc43a14e14a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:00fea9e913dd24612011fa7235fa2ed89ac3a2640280d586566ce45b96f83c1a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19658150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e9610a4453bfe2c025a2edc904a0c7a28fc0bf61239877b85fccc20f91db70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 11 May 2019 00:07:03 GMT
ADD file:a86aea1f3a7d68f6ae03397b99ea77f2e9ee901c5c59e59f76f93adbb4035913 in / 
# Sat, 11 May 2019 00:07:03 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2019 22:19:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 May 2019 22:19:30 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 May 2019 22:31:48 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 24 May 2019 22:31:53 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 May 2019 22:31:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 24 May 2019 22:31:53 GMT
EXPOSE 9092
# Fri, 24 May 2019 22:31:53 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 24 May 2019 22:31:53 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 24 May 2019 22:31:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 May 2019 22:31:54 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e7c96db7181be991f19a9fb6975cdbbd73c65f4a2681348e63a141a2192a5f10`  
		Last Modified: Sat, 11 May 2019 00:07:31 GMT  
		Size: 2.8 MB (2757034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f159e68d94418a67508380d165c862e99b062f7e750d89b6878e7cfa18e8b8`  
		Last Modified: Fri, 24 May 2019 22:20:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb049fef605a954d4e94d7b181b78533f2ab3971cbcdab85b1f9da9edc148d`  
		Last Modified: Fri, 24 May 2019 22:20:07 GMT  
		Size: 301.9 KB (301889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc8c21d0e2f471ffd4f03adcab0b7428a7101e63ad00d0d6242a66c12bdda17`  
		Last Modified: Fri, 24 May 2019 22:32:17 GMT  
		Size: 16.6 MB (16598620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c4bf982dd65a145748a2311ef3a869b8536146b2b9ef4b74a3639b5c02643c`  
		Last Modified: Fri, 24 May 2019 22:32:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24814fe3b7f13d09e864942f67d73cad3074768c1d05e2db02101712dd85cc01`  
		Last Modified: Fri, 24 May 2019 22:32:13 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:5b377752983e68e39b3bf0b7b54f6e939f3e4cd74a186cdd3ce3fc43a14e14a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:00fea9e913dd24612011fa7235fa2ed89ac3a2640280d586566ce45b96f83c1a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19658150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e9610a4453bfe2c025a2edc904a0c7a28fc0bf61239877b85fccc20f91db70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 11 May 2019 00:07:03 GMT
ADD file:a86aea1f3a7d68f6ae03397b99ea77f2e9ee901c5c59e59f76f93adbb4035913 in / 
# Sat, 11 May 2019 00:07:03 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2019 22:19:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 May 2019 22:19:30 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 May 2019 22:31:48 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 24 May 2019 22:31:53 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 May 2019 22:31:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 24 May 2019 22:31:53 GMT
EXPOSE 9092
# Fri, 24 May 2019 22:31:53 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 24 May 2019 22:31:53 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 24 May 2019 22:31:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 May 2019 22:31:54 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e7c96db7181be991f19a9fb6975cdbbd73c65f4a2681348e63a141a2192a5f10`  
		Last Modified: Sat, 11 May 2019 00:07:31 GMT  
		Size: 2.8 MB (2757034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f159e68d94418a67508380d165c862e99b062f7e750d89b6878e7cfa18e8b8`  
		Last Modified: Fri, 24 May 2019 22:20:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb049fef605a954d4e94d7b181b78533f2ab3971cbcdab85b1f9da9edc148d`  
		Last Modified: Fri, 24 May 2019 22:20:07 GMT  
		Size: 301.9 KB (301889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc8c21d0e2f471ffd4f03adcab0b7428a7101e63ad00d0d6242a66c12bdda17`  
		Last Modified: Fri, 24 May 2019 22:32:17 GMT  
		Size: 16.6 MB (16598620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c4bf982dd65a145748a2311ef3a869b8536146b2b9ef4b74a3639b5c02643c`  
		Last Modified: Fri, 24 May 2019 22:32:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24814fe3b7f13d09e864942f67d73cad3074768c1d05e2db02101712dd85cc01`  
		Last Modified: Fri, 24 May 2019 22:32:13 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:c9d3d7529432e913d57c82c973cc2d7f6a9162540b1588407808d62ac6ce21dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:bb13d1d4c1a0efa88bd8dee59679e775db9eebe23099c7cc169daf6413dbf4c7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106539713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4a14da8f4b7bfc425d39f9195a865154fe7296095fd78016ea487675b532a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:26:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 06:26:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:26:27 GMT
ENV KAPACITOR_VERSION=1.5.3
# Sun, 29 Dec 2019 06:26:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:26:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 06:26:31 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 06:26:32 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 06:26:32 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 06:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:26:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54eac68a8c25638e1bfd43b2780191c95eda5f66706d58161f9c254283bbc12`  
		Last Modified: Sun, 29 Dec 2019 06:26:45 GMT  
		Size: 13.1 MB (13086759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ea20cbb970f30a2c63fcaa1eb4ad0c4ca4f87be733a557ad2d068cfdab808`  
		Last Modified: Sun, 29 Dec 2019 06:26:44 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9551c5d9922a2347f30fb5070eacf8d0df8e77cc5be9367c3611bf97fbe57089`  
		Last Modified: Sun, 29 Dec 2019 06:27:01 GMT  
		Size: 32.9 MB (32931645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2892f438e3c2bf60e9ac03347df7bb579602ce35ad6ca8b30d5efec46feac7`  
		Last Modified: Sun, 29 Dec 2019 06:26:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7133396cf6a11490bd0935adafbcad0ee8bfb8addbae82d47d92946dae04d37`  
		Last Modified: Sun, 29 Dec 2019 06:26:56 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:2c0580c569acb93b27fcce93f4193a7eca542aee3682be706b6cf38cfb143268
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99690791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce65d05f88cece223fd46d86b18adeec6c054c422e4406854d56ac34ab38f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:34:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 28 Dec 2019 22:34:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:34:42 GMT
ENV KAPACITOR_VERSION=1.5.3
# Sat, 28 Dec 2019 22:34:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:34:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 28 Dec 2019 22:34:54 GMT
EXPOSE 9092
# Sat, 28 Dec 2019 22:34:54 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 28 Dec 2019 22:34:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 28 Dec 2019 22:34:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:34:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0884195a19c3699ef8c01d1729c1d3961aab5516da4e144c15a158dbeefa18f4`  
		Last Modified: Sat, 28 Dec 2019 22:35:12 GMT  
		Size: 13.3 MB (13256456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e60aaff33912d1472d4b2aea78d7892382813574a8d54017328194c24f19f0d`  
		Last Modified: Sat, 28 Dec 2019 22:35:10 GMT  
		Size: 2.8 KB (2807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1805874c33e9147e40a4c018f0e9424782332ba033c0a595c85494c89dec2377`  
		Last Modified: Sat, 28 Dec 2019 22:35:32 GMT  
		Size: 30.9 MB (30906021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125e8f17a1331ed8660d0e1947091df0e205606db316dcb35338931821dfb1c5`  
		Last Modified: Sat, 28 Dec 2019 22:35:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cebe2c7a671f29bb2d241caf55a9fb3e45c4a0960c570091dd5c4dad3626b83`  
		Last Modified: Sat, 28 Dec 2019 22:35:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:dc3f87863789d3b4b2e62ca8ae8d0e08d2d95fdd5b5615cad707e7370e3ae233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100712725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd82db3f185cafacf0bc3af594e5f3b34bb1b36ddff7a25f5618c3d05b089ad4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:15:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 00:32:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 00:32:44 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 00:33:38 GMT
ENV KAPACITOR_VERSION=1.5.3
# Sun, 29 Dec 2019 00:33:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 00:33:48 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 00:33:50 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 00:33:53 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 00:33:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 00:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 00:34:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f31062581dadb1f69c43e9441040dd46788bf13ae51f20c66929fac82b506b`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 9.7 MB (9748258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62337a296a607f48a5dc3a7c07639360d98e0e78982ca8e459c832719012f12`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 4.1 MB (4094448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58545439b4e40db5dab6e07f70e26ad455d4de4843cb02c2f7f2aa6305b9a626`  
		Last Modified: Sun, 29 Dec 2019 00:34:16 GMT  
		Size: 12.8 MB (12794461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6bfca4f9e2f8f017e83cf18a76193e51f5c4714e487d978f5e508416626293`  
		Last Modified: Sun, 29 Dec 2019 00:34:14 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b3ab7020d61eac197efa862d1d59f7a97b08889dc398fb7a4c9bf1e9b5b72a`  
		Last Modified: Sun, 29 Dec 2019 00:34:34 GMT  
		Size: 30.9 MB (30905823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5267a0e6195bc4cf194060dba159ad76647a8d2a0550087b1e75489b2f5e78d`  
		Last Modified: Sun, 29 Dec 2019 00:34:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f725c845780a23865905068282855d72fe737c2d352e9bc418507b5f5935a9`  
		Last Modified: Sun, 29 Dec 2019 00:34:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.3`

```console
$ docker pull kapacitor@sha256:c9d3d7529432e913d57c82c973cc2d7f6a9162540b1588407808d62ac6ce21dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.3` - linux; amd64

```console
$ docker pull kapacitor@sha256:bb13d1d4c1a0efa88bd8dee59679e775db9eebe23099c7cc169daf6413dbf4c7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106539713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4a14da8f4b7bfc425d39f9195a865154fe7296095fd78016ea487675b532a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:26:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 06:26:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:26:27 GMT
ENV KAPACITOR_VERSION=1.5.3
# Sun, 29 Dec 2019 06:26:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:26:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 06:26:31 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 06:26:32 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 06:26:32 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 06:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:26:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54eac68a8c25638e1bfd43b2780191c95eda5f66706d58161f9c254283bbc12`  
		Last Modified: Sun, 29 Dec 2019 06:26:45 GMT  
		Size: 13.1 MB (13086759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ea20cbb970f30a2c63fcaa1eb4ad0c4ca4f87be733a557ad2d068cfdab808`  
		Last Modified: Sun, 29 Dec 2019 06:26:44 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9551c5d9922a2347f30fb5070eacf8d0df8e77cc5be9367c3611bf97fbe57089`  
		Last Modified: Sun, 29 Dec 2019 06:27:01 GMT  
		Size: 32.9 MB (32931645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2892f438e3c2bf60e9ac03347df7bb579602ce35ad6ca8b30d5efec46feac7`  
		Last Modified: Sun, 29 Dec 2019 06:26:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7133396cf6a11490bd0935adafbcad0ee8bfb8addbae82d47d92946dae04d37`  
		Last Modified: Sun, 29 Dec 2019 06:26:56 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.3` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:2c0580c569acb93b27fcce93f4193a7eca542aee3682be706b6cf38cfb143268
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99690791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce65d05f88cece223fd46d86b18adeec6c054c422e4406854d56ac34ab38f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:34:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 28 Dec 2019 22:34:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:34:42 GMT
ENV KAPACITOR_VERSION=1.5.3
# Sat, 28 Dec 2019 22:34:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:34:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 28 Dec 2019 22:34:54 GMT
EXPOSE 9092
# Sat, 28 Dec 2019 22:34:54 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 28 Dec 2019 22:34:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 28 Dec 2019 22:34:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:34:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0884195a19c3699ef8c01d1729c1d3961aab5516da4e144c15a158dbeefa18f4`  
		Last Modified: Sat, 28 Dec 2019 22:35:12 GMT  
		Size: 13.3 MB (13256456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e60aaff33912d1472d4b2aea78d7892382813574a8d54017328194c24f19f0d`  
		Last Modified: Sat, 28 Dec 2019 22:35:10 GMT  
		Size: 2.8 KB (2807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1805874c33e9147e40a4c018f0e9424782332ba033c0a595c85494c89dec2377`  
		Last Modified: Sat, 28 Dec 2019 22:35:32 GMT  
		Size: 30.9 MB (30906021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125e8f17a1331ed8660d0e1947091df0e205606db316dcb35338931821dfb1c5`  
		Last Modified: Sat, 28 Dec 2019 22:35:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cebe2c7a671f29bb2d241caf55a9fb3e45c4a0960c570091dd5c4dad3626b83`  
		Last Modified: Sat, 28 Dec 2019 22:35:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.3` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:dc3f87863789d3b4b2e62ca8ae8d0e08d2d95fdd5b5615cad707e7370e3ae233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100712725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd82db3f185cafacf0bc3af594e5f3b34bb1b36ddff7a25f5618c3d05b089ad4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:15:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 00:32:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 00:32:44 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 00:33:38 GMT
ENV KAPACITOR_VERSION=1.5.3
# Sun, 29 Dec 2019 00:33:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 00:33:48 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 00:33:50 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 00:33:53 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 00:33:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 00:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 00:34:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f31062581dadb1f69c43e9441040dd46788bf13ae51f20c66929fac82b506b`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 9.7 MB (9748258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62337a296a607f48a5dc3a7c07639360d98e0e78982ca8e459c832719012f12`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 4.1 MB (4094448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58545439b4e40db5dab6e07f70e26ad455d4de4843cb02c2f7f2aa6305b9a626`  
		Last Modified: Sun, 29 Dec 2019 00:34:16 GMT  
		Size: 12.8 MB (12794461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6bfca4f9e2f8f017e83cf18a76193e51f5c4714e487d978f5e508416626293`  
		Last Modified: Sun, 29 Dec 2019 00:34:14 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b3ab7020d61eac197efa862d1d59f7a97b08889dc398fb7a4c9bf1e9b5b72a`  
		Last Modified: Sun, 29 Dec 2019 00:34:34 GMT  
		Size: 30.9 MB (30905823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5267a0e6195bc4cf194060dba159ad76647a8d2a0550087b1e75489b2f5e78d`  
		Last Modified: Sun, 29 Dec 2019 00:34:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f725c845780a23865905068282855d72fe737c2d352e9bc418507b5f5935a9`  
		Last Modified: Sun, 29 Dec 2019 00:34:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.3-alpine`

```console
$ docker pull kapacitor@sha256:0fb078ebac1cd437f7b711ed0de482d13d383dcf993e70cb4d95111f2cc596c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.3-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c2d93b8b669734d7832c8c8b1fbf1c54545426a9c77dac3ac6878f3ba7a23a8d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22501057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a63b9d348dff833ae83cb6e3b2aa1a5e66ce80da45964331b190a8734efbfc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 11 May 2019 00:07:03 GMT
ADD file:a86aea1f3a7d68f6ae03397b99ea77f2e9ee901c5c59e59f76f93adbb4035913 in / 
# Sat, 11 May 2019 00:07:03 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2019 22:19:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 May 2019 22:19:30 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 19 Jun 2019 20:23:25 GMT
ENV KAPACITOR_VERSION=1.5.3
# Wed, 19 Jun 2019 20:23:30 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 19 Jun 2019 20:23:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 19 Jun 2019 20:23:30 GMT
EXPOSE 9092
# Wed, 19 Jun 2019 20:23:31 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 19 Jun 2019 20:23:31 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 19 Jun 2019 20:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Jun 2019 20:23:31 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e7c96db7181be991f19a9fb6975cdbbd73c65f4a2681348e63a141a2192a5f10`  
		Last Modified: Sat, 11 May 2019 00:07:31 GMT  
		Size: 2.8 MB (2757034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f159e68d94418a67508380d165c862e99b062f7e750d89b6878e7cfa18e8b8`  
		Last Modified: Fri, 24 May 2019 22:20:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb049fef605a954d4e94d7b181b78533f2ab3971cbcdab85b1f9da9edc148d`  
		Last Modified: Fri, 24 May 2019 22:20:07 GMT  
		Size: 301.9 KB (301889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a94d867901a706fecc32a09a04d6f70584e689518f9c2577ef2a6d9de8c9a11`  
		Last Modified: Wed, 19 Jun 2019 20:23:59 GMT  
		Size: 19.4 MB (19441528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce706f5a4090e7a87c84b8abed8e83eab5cd4611c209897ef58a7d4c20780f1`  
		Last Modified: Wed, 19 Jun 2019 20:23:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304ae320287f2a2ca011b36d8320e54927e91713da9e183f9f276888bbe70562`  
		Last Modified: Wed, 19 Jun 2019 20:23:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:0fb078ebac1cd437f7b711ed0de482d13d383dcf993e70cb4d95111f2cc596c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c2d93b8b669734d7832c8c8b1fbf1c54545426a9c77dac3ac6878f3ba7a23a8d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22501057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a63b9d348dff833ae83cb6e3b2aa1a5e66ce80da45964331b190a8734efbfc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 11 May 2019 00:07:03 GMT
ADD file:a86aea1f3a7d68f6ae03397b99ea77f2e9ee901c5c59e59f76f93adbb4035913 in / 
# Sat, 11 May 2019 00:07:03 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2019 22:19:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 May 2019 22:19:30 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 19 Jun 2019 20:23:25 GMT
ENV KAPACITOR_VERSION=1.5.3
# Wed, 19 Jun 2019 20:23:30 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 19 Jun 2019 20:23:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 19 Jun 2019 20:23:30 GMT
EXPOSE 9092
# Wed, 19 Jun 2019 20:23:31 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 19 Jun 2019 20:23:31 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 19 Jun 2019 20:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Jun 2019 20:23:31 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e7c96db7181be991f19a9fb6975cdbbd73c65f4a2681348e63a141a2192a5f10`  
		Last Modified: Sat, 11 May 2019 00:07:31 GMT  
		Size: 2.8 MB (2757034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f159e68d94418a67508380d165c862e99b062f7e750d89b6878e7cfa18e8b8`  
		Last Modified: Fri, 24 May 2019 22:20:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb049fef605a954d4e94d7b181b78533f2ab3971cbcdab85b1f9da9edc148d`  
		Last Modified: Fri, 24 May 2019 22:20:07 GMT  
		Size: 301.9 KB (301889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a94d867901a706fecc32a09a04d6f70584e689518f9c2577ef2a6d9de8c9a11`  
		Last Modified: Wed, 19 Jun 2019 20:23:59 GMT  
		Size: 19.4 MB (19441528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce706f5a4090e7a87c84b8abed8e83eab5cd4611c209897ef58a7d4c20780f1`  
		Last Modified: Wed, 19 Jun 2019 20:23:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304ae320287f2a2ca011b36d8320e54927e91713da9e183f9f276888bbe70562`  
		Last Modified: Wed, 19 Jun 2019 20:23:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:0fb078ebac1cd437f7b711ed0de482d13d383dcf993e70cb4d95111f2cc596c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c2d93b8b669734d7832c8c8b1fbf1c54545426a9c77dac3ac6878f3ba7a23a8d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22501057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a63b9d348dff833ae83cb6e3b2aa1a5e66ce80da45964331b190a8734efbfc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 11 May 2019 00:07:03 GMT
ADD file:a86aea1f3a7d68f6ae03397b99ea77f2e9ee901c5c59e59f76f93adbb4035913 in / 
# Sat, 11 May 2019 00:07:03 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2019 22:19:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 May 2019 22:19:30 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 19 Jun 2019 20:23:25 GMT
ENV KAPACITOR_VERSION=1.5.3
# Wed, 19 Jun 2019 20:23:30 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 19 Jun 2019 20:23:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 19 Jun 2019 20:23:30 GMT
EXPOSE 9092
# Wed, 19 Jun 2019 20:23:31 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 19 Jun 2019 20:23:31 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 19 Jun 2019 20:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Jun 2019 20:23:31 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e7c96db7181be991f19a9fb6975cdbbd73c65f4a2681348e63a141a2192a5f10`  
		Last Modified: Sat, 11 May 2019 00:07:31 GMT  
		Size: 2.8 MB (2757034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f159e68d94418a67508380d165c862e99b062f7e750d89b6878e7cfa18e8b8`  
		Last Modified: Fri, 24 May 2019 22:20:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb049fef605a954d4e94d7b181b78533f2ab3971cbcdab85b1f9da9edc148d`  
		Last Modified: Fri, 24 May 2019 22:20:07 GMT  
		Size: 301.9 KB (301889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a94d867901a706fecc32a09a04d6f70584e689518f9c2577ef2a6d9de8c9a11`  
		Last Modified: Wed, 19 Jun 2019 20:23:59 GMT  
		Size: 19.4 MB (19441528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce706f5a4090e7a87c84b8abed8e83eab5cd4611c209897ef58a7d4c20780f1`  
		Last Modified: Wed, 19 Jun 2019 20:23:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304ae320287f2a2ca011b36d8320e54927e91713da9e183f9f276888bbe70562`  
		Last Modified: Wed, 19 Jun 2019 20:23:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:c9d3d7529432e913d57c82c973cc2d7f6a9162540b1588407808d62ac6ce21dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:bb13d1d4c1a0efa88bd8dee59679e775db9eebe23099c7cc169daf6413dbf4c7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106539713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4a14da8f4b7bfc425d39f9195a865154fe7296095fd78016ea487675b532a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:26:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 06:26:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:26:27 GMT
ENV KAPACITOR_VERSION=1.5.3
# Sun, 29 Dec 2019 06:26:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:26:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 06:26:31 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 06:26:32 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 06:26:32 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 06:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:26:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54eac68a8c25638e1bfd43b2780191c95eda5f66706d58161f9c254283bbc12`  
		Last Modified: Sun, 29 Dec 2019 06:26:45 GMT  
		Size: 13.1 MB (13086759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ea20cbb970f30a2c63fcaa1eb4ad0c4ca4f87be733a557ad2d068cfdab808`  
		Last Modified: Sun, 29 Dec 2019 06:26:44 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9551c5d9922a2347f30fb5070eacf8d0df8e77cc5be9367c3611bf97fbe57089`  
		Last Modified: Sun, 29 Dec 2019 06:27:01 GMT  
		Size: 32.9 MB (32931645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2892f438e3c2bf60e9ac03347df7bb579602ce35ad6ca8b30d5efec46feac7`  
		Last Modified: Sun, 29 Dec 2019 06:26:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7133396cf6a11490bd0935adafbcad0ee8bfb8addbae82d47d92946dae04d37`  
		Last Modified: Sun, 29 Dec 2019 06:26:56 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:2c0580c569acb93b27fcce93f4193a7eca542aee3682be706b6cf38cfb143268
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99690791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce65d05f88cece223fd46d86b18adeec6c054c422e4406854d56ac34ab38f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:34:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 28 Dec 2019 22:34:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:34:42 GMT
ENV KAPACITOR_VERSION=1.5.3
# Sat, 28 Dec 2019 22:34:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:34:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 28 Dec 2019 22:34:54 GMT
EXPOSE 9092
# Sat, 28 Dec 2019 22:34:54 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 28 Dec 2019 22:34:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 28 Dec 2019 22:34:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:34:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0884195a19c3699ef8c01d1729c1d3961aab5516da4e144c15a158dbeefa18f4`  
		Last Modified: Sat, 28 Dec 2019 22:35:12 GMT  
		Size: 13.3 MB (13256456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e60aaff33912d1472d4b2aea78d7892382813574a8d54017328194c24f19f0d`  
		Last Modified: Sat, 28 Dec 2019 22:35:10 GMT  
		Size: 2.8 KB (2807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1805874c33e9147e40a4c018f0e9424782332ba033c0a595c85494c89dec2377`  
		Last Modified: Sat, 28 Dec 2019 22:35:32 GMT  
		Size: 30.9 MB (30906021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125e8f17a1331ed8660d0e1947091df0e205606db316dcb35338931821dfb1c5`  
		Last Modified: Sat, 28 Dec 2019 22:35:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cebe2c7a671f29bb2d241caf55a9fb3e45c4a0960c570091dd5c4dad3626b83`  
		Last Modified: Sat, 28 Dec 2019 22:35:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:dc3f87863789d3b4b2e62ca8ae8d0e08d2d95fdd5b5615cad707e7370e3ae233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100712725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd82db3f185cafacf0bc3af594e5f3b34bb1b36ddff7a25f5618c3d05b089ad4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:15:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 00:32:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sun, 29 Dec 2019 00:32:44 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 00:33:38 GMT
ENV KAPACITOR_VERSION=1.5.3
# Sun, 29 Dec 2019 00:33:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 00:33:48 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sun, 29 Dec 2019 00:33:50 GMT
EXPOSE 9092
# Sun, 29 Dec 2019 00:33:53 GMT
VOLUME [/var/lib/kapacitor]
# Sun, 29 Dec 2019 00:33:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sun, 29 Dec 2019 00:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 00:34:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f31062581dadb1f69c43e9441040dd46788bf13ae51f20c66929fac82b506b`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 9.7 MB (9748258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62337a296a607f48a5dc3a7c07639360d98e0e78982ca8e459c832719012f12`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 4.1 MB (4094448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58545439b4e40db5dab6e07f70e26ad455d4de4843cb02c2f7f2aa6305b9a626`  
		Last Modified: Sun, 29 Dec 2019 00:34:16 GMT  
		Size: 12.8 MB (12794461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6bfca4f9e2f8f017e83cf18a76193e51f5c4714e487d978f5e508416626293`  
		Last Modified: Sun, 29 Dec 2019 00:34:14 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b3ab7020d61eac197efa862d1d59f7a97b08889dc398fb7a4c9bf1e9b5b72a`  
		Last Modified: Sun, 29 Dec 2019 00:34:34 GMT  
		Size: 30.9 MB (30905823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5267a0e6195bc4cf194060dba159ad76647a8d2a0550087b1e75489b2f5e78d`  
		Last Modified: Sun, 29 Dec 2019 00:34:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f725c845780a23865905068282855d72fe737c2d352e9bc418507b5f5935a9`  
		Last Modified: Sun, 29 Dec 2019 00:34:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
