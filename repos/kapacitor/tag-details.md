<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:1.5.8`](#kapacitor158)
-	[`kapacitor:1.5.8-alpine`](#kapacitor158-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:56b4060248e5ffe421518e85e8651fcbe4e4861445a81eeac6573309369bf676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:1e64e6aeda6cecfa26df9db8ee87f3e216fd1277743e8d88708cfcb4a102dc28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96970580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a408da54922b898bf26ffd6ad832188bf396265af5462789458d590ab0391a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:31:52 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 20:31:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 20:31:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:31:56 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:31:56 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:31:56 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:31:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:31:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473f39bb5ac5870cdede8897911c55fe1279666c3ddf7d3147c598ab93a3337c`  
		Last Modified: Sat, 27 Mar 2021 20:32:32 GMT  
		Size: 22.7 MB (22695441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb819cb9874f896ac76f6b558815ba5e4554e4c033fd5aaf9c31b688b1080b`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a817a17222887d9a00748d2d75db3f39d72607ea9318427186136ae3ae54c`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:ccecc2174867a4b78d7c70cc924137164e342aceb5902cf3c8735dc915f69d8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90734598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0797aa45760da35f5deb3683fdb2719ad615676454177717e71307d58c501f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:15 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 09:07:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:27 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:07:28 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:07:28 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:07:30 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:07:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:07:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360770c5a31ae0607cbf09cd7d020eaecfdfa816afc6035c48600e9ffcd3d53b`  
		Last Modified: Sat, 27 Mar 2021 09:08:32 GMT  
		Size: 21.3 MB (21309019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c416ea00897389d4739bfb9d2cd098ffb86fe3293471bfc7f6a6f890bb04e31`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd21dd5fb4748e21e4c36bf5da2b22698ba5ec1ef4d20220fe59cd8c7f1305f`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:cf655c493b63d911afd3daf70701181e033bb9a20e0861c5572976008a3d4351
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91754165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713750092db95d23c53f6e30ffe5e294b7858620ce42a8b591c52730658aa2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:44:15 GMT
ADD file:cf753fedc426819aa5f93f4ad934479efd8fbf024b408627239b77ddc5223108 in / 
# Fri, 26 Mar 2021 15:44:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:21:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 23:47:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 23:47:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 23:47:23 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 23:47:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 23:47:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 23:47:30 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 23:47:30 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 23:47:31 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 23:47:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 23:47:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1a0736e738921f2c70c8ce48d5ba8b042279c41c41f32a1af43a6cbd299f6d89`  
		Last Modified: Fri, 26 Mar 2021 15:50:55 GMT  
		Size: 43.2 MB (43176405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c963a30dbe4f7f47cba7603121834cb6b6f206d9c25e8a96df41cfd42eab3e`  
		Last Modified: Sat, 27 Mar 2021 04:30:49 GMT  
		Size: 10.2 MB (10201048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97078da83c94ce9db743f96c02e8deaf24987dd4e94aced6c6b5ceb860b8f8ac`  
		Last Modified: Sat, 27 Mar 2021 04:30:47 GMT  
		Size: 4.1 MB (4096666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261e51104922fc98e8cfda60b3facdb439cab292dae4e0369fb8fffc0b1fd201`  
		Last Modified: Sat, 27 Mar 2021 23:48:05 GMT  
		Size: 13.0 MB (12968150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c744e842337b47b39ce131e84dd273e87f1ec810aa84a982428daefab495bb`  
		Last Modified: Sat, 27 Mar 2021 23:48:03 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0125d76c740fdfbea55acaa8009b3d405d9f8e3a42732f4686e8a0851b007a2`  
		Last Modified: Sat, 27 Mar 2021 23:48:10 GMT  
		Size: 21.3 MB (21308584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa3d63b9c0d8ac7671231861a1d879d2ef2e4074be8ead9f6956c8942607e79`  
		Last Modified: Sat, 27 Mar 2021 23:48:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3298ed9e382a991d5a04504d9ab915cd319404868bae809318c6fecc92c81c6`  
		Last Modified: Sat, 27 Mar 2021 23:48:03 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:54a6209f0269a3c3dcdaa302c2d0649fe8db1dcdd3aa7dd84731546cf65ed45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b550e6807fc912340d2801c376672a1a11430367cdfdfe37faa6e2208fcbd75a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19679814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed38b5e46c1e806aa08222730a72f63c2ea8cc5b8369089ca2b8b548aa475d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:22:49 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 26 Mar 2021 08:22:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:22:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:22:54 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:22:54 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:22:54 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:22:54 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dc843fb1f362c9d9f9a5cb89ddcbc78e3ad79f2ae8bd830fe5f679d0c386ed`  
		Last Modified: Fri, 26 Mar 2021 08:23:29 GMT  
		Size: 16.6 MB (16598543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e875139b687500fa7b3e558749354b4e74fd98b31d035ee8c59638d90aeeeeb`  
		Last Modified: Fri, 26 Mar 2021 08:23:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5703f1fbcb9d90bb8ff7ba69f8c5ed12b12f2c7d42263356b3289a43239fc3`  
		Last Modified: Fri, 26 Mar 2021 08:23:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:56b4060248e5ffe421518e85e8651fcbe4e4861445a81eeac6573309369bf676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:1e64e6aeda6cecfa26df9db8ee87f3e216fd1277743e8d88708cfcb4a102dc28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96970580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a408da54922b898bf26ffd6ad832188bf396265af5462789458d590ab0391a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:31:52 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 20:31:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 20:31:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:31:56 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:31:56 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:31:56 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:31:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:31:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473f39bb5ac5870cdede8897911c55fe1279666c3ddf7d3147c598ab93a3337c`  
		Last Modified: Sat, 27 Mar 2021 20:32:32 GMT  
		Size: 22.7 MB (22695441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb819cb9874f896ac76f6b558815ba5e4554e4c033fd5aaf9c31b688b1080b`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a817a17222887d9a00748d2d75db3f39d72607ea9318427186136ae3ae54c`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:ccecc2174867a4b78d7c70cc924137164e342aceb5902cf3c8735dc915f69d8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90734598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0797aa45760da35f5deb3683fdb2719ad615676454177717e71307d58c501f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:15 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 09:07:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:27 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:07:28 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:07:28 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:07:30 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:07:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:07:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360770c5a31ae0607cbf09cd7d020eaecfdfa816afc6035c48600e9ffcd3d53b`  
		Last Modified: Sat, 27 Mar 2021 09:08:32 GMT  
		Size: 21.3 MB (21309019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c416ea00897389d4739bfb9d2cd098ffb86fe3293471bfc7f6a6f890bb04e31`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd21dd5fb4748e21e4c36bf5da2b22698ba5ec1ef4d20220fe59cd8c7f1305f`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:cf655c493b63d911afd3daf70701181e033bb9a20e0861c5572976008a3d4351
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91754165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713750092db95d23c53f6e30ffe5e294b7858620ce42a8b591c52730658aa2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:44:15 GMT
ADD file:cf753fedc426819aa5f93f4ad934479efd8fbf024b408627239b77ddc5223108 in / 
# Fri, 26 Mar 2021 15:44:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:21:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 23:47:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 23:47:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 23:47:23 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 23:47:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 23:47:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 23:47:30 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 23:47:30 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 23:47:31 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 23:47:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 23:47:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1a0736e738921f2c70c8ce48d5ba8b042279c41c41f32a1af43a6cbd299f6d89`  
		Last Modified: Fri, 26 Mar 2021 15:50:55 GMT  
		Size: 43.2 MB (43176405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c963a30dbe4f7f47cba7603121834cb6b6f206d9c25e8a96df41cfd42eab3e`  
		Last Modified: Sat, 27 Mar 2021 04:30:49 GMT  
		Size: 10.2 MB (10201048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97078da83c94ce9db743f96c02e8deaf24987dd4e94aced6c6b5ceb860b8f8ac`  
		Last Modified: Sat, 27 Mar 2021 04:30:47 GMT  
		Size: 4.1 MB (4096666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261e51104922fc98e8cfda60b3facdb439cab292dae4e0369fb8fffc0b1fd201`  
		Last Modified: Sat, 27 Mar 2021 23:48:05 GMT  
		Size: 13.0 MB (12968150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c744e842337b47b39ce131e84dd273e87f1ec810aa84a982428daefab495bb`  
		Last Modified: Sat, 27 Mar 2021 23:48:03 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0125d76c740fdfbea55acaa8009b3d405d9f8e3a42732f4686e8a0851b007a2`  
		Last Modified: Sat, 27 Mar 2021 23:48:10 GMT  
		Size: 21.3 MB (21308584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa3d63b9c0d8ac7671231861a1d879d2ef2e4074be8ead9f6956c8942607e79`  
		Last Modified: Sat, 27 Mar 2021 23:48:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3298ed9e382a991d5a04504d9ab915cd319404868bae809318c6fecc92c81c6`  
		Last Modified: Sat, 27 Mar 2021 23:48:03 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:54a6209f0269a3c3dcdaa302c2d0649fe8db1dcdd3aa7dd84731546cf65ed45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b550e6807fc912340d2801c376672a1a11430367cdfdfe37faa6e2208fcbd75a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19679814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed38b5e46c1e806aa08222730a72f63c2ea8cc5b8369089ca2b8b548aa475d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:22:49 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 26 Mar 2021 08:22:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:22:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:22:54 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:22:54 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:22:54 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:22:54 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dc843fb1f362c9d9f9a5cb89ddcbc78e3ad79f2ae8bd830fe5f679d0c386ed`  
		Last Modified: Fri, 26 Mar 2021 08:23:29 GMT  
		Size: 16.6 MB (16598543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e875139b687500fa7b3e558749354b4e74fd98b31d035ee8c59638d90aeeeeb`  
		Last Modified: Fri, 26 Mar 2021 08:23:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5703f1fbcb9d90bb8ff7ba69f8c5ed12b12f2c7d42263356b3289a43239fc3`  
		Last Modified: Fri, 26 Mar 2021 08:23:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:3fc0a8cb55f7993bf0ad12082cb74b1d0e8f6465b6371f946693a785dc20319b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:3ab61e2059a4f3cafacff7d1cfdc3d4d7d2911f61ced6468fef57a1c08e72ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111449500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada42dea1083fd4a68ed700a926cafbed4dec691e19ad952d054b58ee462d467`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:32:02 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 20:32:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 20:32:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:32:08 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:32:08 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:32:08 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:32:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:32:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bf00bbc3dfb229dd261e340cf51cd7ab2c521606bf33a31c0151957364fb66`  
		Last Modified: Sat, 27 Mar 2021 20:32:48 GMT  
		Size: 37.2 MB (37174360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e093880828ab1d78f8852129cd98780c9b79e7f1f029b830991e8469b145b21`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c239f527a9508c7200c46a24012866348a320a71d4df24fad6fea341f793e679`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:b906902169272e864f480f9086430f53c626dc49250202c66aa2d5fe4c7833cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104164159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7abeabbf2891b8bccfcf54b68a002c8132809ae3da54988d773b3013dffc2038`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:46 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 09:07:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:08:01 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:08:02 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:08:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:08:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a314e91b9ff7f5d05bb6d8035d6ca93b5cc938ae5339ce34e4c6206ae42995b`  
		Last Modified: Sat, 27 Mar 2021 09:08:48 GMT  
		Size: 34.7 MB (34738582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4220b10e3575373f9809be75ac373fd7d3ed227ed82a1a35a48482d78666fc`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664b33bbc1108e9b0e1dcb52fea68f46fd64ac4bdde359973d3a2782508b5ff3`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:96b61ed9e099f70d605ce003800ebfc6d795cae3bc1c8160513eb356b3a2dae8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104976110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0668ff37c1069274906f210e54abc661736c4a0a36f187bc6269e78f617e3d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:44:15 GMT
ADD file:cf753fedc426819aa5f93f4ad934479efd8fbf024b408627239b77ddc5223108 in / 
# Fri, 26 Mar 2021 15:44:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:21:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 23:47:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 23:47:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 23:47:41 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 23:47:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 23:47:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 23:47:48 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 23:47:48 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 23:47:49 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 23:47:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 23:47:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1a0736e738921f2c70c8ce48d5ba8b042279c41c41f32a1af43a6cbd299f6d89`  
		Last Modified: Fri, 26 Mar 2021 15:50:55 GMT  
		Size: 43.2 MB (43176405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c963a30dbe4f7f47cba7603121834cb6b6f206d9c25e8a96df41cfd42eab3e`  
		Last Modified: Sat, 27 Mar 2021 04:30:49 GMT  
		Size: 10.2 MB (10201048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97078da83c94ce9db743f96c02e8deaf24987dd4e94aced6c6b5ceb860b8f8ac`  
		Last Modified: Sat, 27 Mar 2021 04:30:47 GMT  
		Size: 4.1 MB (4096666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261e51104922fc98e8cfda60b3facdb439cab292dae4e0369fb8fffc0b1fd201`  
		Last Modified: Sat, 27 Mar 2021 23:48:05 GMT  
		Size: 13.0 MB (12968150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c744e842337b47b39ce131e84dd273e87f1ec810aa84a982428daefab495bb`  
		Last Modified: Sat, 27 Mar 2021 23:48:03 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f0fc49d8045dd78f0dd563618df408b7f15a87ac48807b4260c8e7a58a4cb`  
		Last Modified: Sat, 27 Mar 2021 23:48:23 GMT  
		Size: 34.5 MB (34530530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab540866ae425c35d3013643752b949d4c456be133d3b905c1e0ee34d652b1cc`  
		Last Modified: Sat, 27 Mar 2021 23:48:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a0a5263d418958b889d8c7bb185ecb018a71d0dee3309477db60c2f4a9888b`  
		Last Modified: Sat, 27 Mar 2021 23:48:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:684a895ed468b04f098a03081339331035942409718bfe72ea1ea2b9660f1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e778dca7174b8237484b939711d1e6cce324c71ab655f31f03ab5dfa1cb0dbef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22598232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51adc0fc1da945b01596c8be1d037467be8b5f0e48bb5f52777b92ee484f2557`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:23:00 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 26 Mar 2021 08:23:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:23:05 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:23:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:23:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:23:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50319ecf6cd5028d57c8a15888eff67a9c5ef9549ff4d40452dd713ad65dc254`  
		Last Modified: Fri, 26 Mar 2021 08:23:48 GMT  
		Size: 19.5 MB (19516959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cce72b7cf74eaf6267dde03d9ddaac716790a02d9af5ac5894b9d7ab414b27d`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba736aa2bc582298f5370c9d3b7b5688b8cfdb37ee0b8292196b72a49574ff1`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.8`

```console
$ docker pull kapacitor@sha256:3fc0a8cb55f7993bf0ad12082cb74b1d0e8f6465b6371f946693a785dc20319b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:3ab61e2059a4f3cafacff7d1cfdc3d4d7d2911f61ced6468fef57a1c08e72ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111449500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada42dea1083fd4a68ed700a926cafbed4dec691e19ad952d054b58ee462d467`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:32:02 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 20:32:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 20:32:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:32:08 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:32:08 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:32:08 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:32:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:32:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bf00bbc3dfb229dd261e340cf51cd7ab2c521606bf33a31c0151957364fb66`  
		Last Modified: Sat, 27 Mar 2021 20:32:48 GMT  
		Size: 37.2 MB (37174360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e093880828ab1d78f8852129cd98780c9b79e7f1f029b830991e8469b145b21`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c239f527a9508c7200c46a24012866348a320a71d4df24fad6fea341f793e679`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.8` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:b906902169272e864f480f9086430f53c626dc49250202c66aa2d5fe4c7833cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104164159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7abeabbf2891b8bccfcf54b68a002c8132809ae3da54988d773b3013dffc2038`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:46 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 09:07:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:08:01 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:08:02 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:08:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:08:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a314e91b9ff7f5d05bb6d8035d6ca93b5cc938ae5339ce34e4c6206ae42995b`  
		Last Modified: Sat, 27 Mar 2021 09:08:48 GMT  
		Size: 34.7 MB (34738582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4220b10e3575373f9809be75ac373fd7d3ed227ed82a1a35a48482d78666fc`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664b33bbc1108e9b0e1dcb52fea68f46fd64ac4bdde359973d3a2782508b5ff3`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:96b61ed9e099f70d605ce003800ebfc6d795cae3bc1c8160513eb356b3a2dae8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104976110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0668ff37c1069274906f210e54abc661736c4a0a36f187bc6269e78f617e3d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:44:15 GMT
ADD file:cf753fedc426819aa5f93f4ad934479efd8fbf024b408627239b77ddc5223108 in / 
# Fri, 26 Mar 2021 15:44:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:21:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 23:47:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 23:47:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 23:47:41 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 23:47:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 23:47:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 23:47:48 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 23:47:48 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 23:47:49 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 23:47:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 23:47:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1a0736e738921f2c70c8ce48d5ba8b042279c41c41f32a1af43a6cbd299f6d89`  
		Last Modified: Fri, 26 Mar 2021 15:50:55 GMT  
		Size: 43.2 MB (43176405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c963a30dbe4f7f47cba7603121834cb6b6f206d9c25e8a96df41cfd42eab3e`  
		Last Modified: Sat, 27 Mar 2021 04:30:49 GMT  
		Size: 10.2 MB (10201048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97078da83c94ce9db743f96c02e8deaf24987dd4e94aced6c6b5ceb860b8f8ac`  
		Last Modified: Sat, 27 Mar 2021 04:30:47 GMT  
		Size: 4.1 MB (4096666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261e51104922fc98e8cfda60b3facdb439cab292dae4e0369fb8fffc0b1fd201`  
		Last Modified: Sat, 27 Mar 2021 23:48:05 GMT  
		Size: 13.0 MB (12968150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c744e842337b47b39ce131e84dd273e87f1ec810aa84a982428daefab495bb`  
		Last Modified: Sat, 27 Mar 2021 23:48:03 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f0fc49d8045dd78f0dd563618df408b7f15a87ac48807b4260c8e7a58a4cb`  
		Last Modified: Sat, 27 Mar 2021 23:48:23 GMT  
		Size: 34.5 MB (34530530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab540866ae425c35d3013643752b949d4c456be133d3b905c1e0ee34d652b1cc`  
		Last Modified: Sat, 27 Mar 2021 23:48:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a0a5263d418958b889d8c7bb185ecb018a71d0dee3309477db60c2f4a9888b`  
		Last Modified: Sat, 27 Mar 2021 23:48:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.8-alpine`

```console
$ docker pull kapacitor@sha256:684a895ed468b04f098a03081339331035942409718bfe72ea1ea2b9660f1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e778dca7174b8237484b939711d1e6cce324c71ab655f31f03ab5dfa1cb0dbef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22598232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51adc0fc1da945b01596c8be1d037467be8b5f0e48bb5f52777b92ee484f2557`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:23:00 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 26 Mar 2021 08:23:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:23:05 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:23:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:23:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:23:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50319ecf6cd5028d57c8a15888eff67a9c5ef9549ff4d40452dd713ad65dc254`  
		Last Modified: Fri, 26 Mar 2021 08:23:48 GMT  
		Size: 19.5 MB (19516959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cce72b7cf74eaf6267dde03d9ddaac716790a02d9af5ac5894b9d7ab414b27d`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba736aa2bc582298f5370c9d3b7b5688b8cfdb37ee0b8292196b72a49574ff1`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:684a895ed468b04f098a03081339331035942409718bfe72ea1ea2b9660f1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e778dca7174b8237484b939711d1e6cce324c71ab655f31f03ab5dfa1cb0dbef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22598232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51adc0fc1da945b01596c8be1d037467be8b5f0e48bb5f52777b92ee484f2557`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:23:00 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 26 Mar 2021 08:23:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:23:05 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:23:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:23:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:23:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50319ecf6cd5028d57c8a15888eff67a9c5ef9549ff4d40452dd713ad65dc254`  
		Last Modified: Fri, 26 Mar 2021 08:23:48 GMT  
		Size: 19.5 MB (19516959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cce72b7cf74eaf6267dde03d9ddaac716790a02d9af5ac5894b9d7ab414b27d`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba736aa2bc582298f5370c9d3b7b5688b8cfdb37ee0b8292196b72a49574ff1`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:3fc0a8cb55f7993bf0ad12082cb74b1d0e8f6465b6371f946693a785dc20319b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:3ab61e2059a4f3cafacff7d1cfdc3d4d7d2911f61ced6468fef57a1c08e72ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111449500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada42dea1083fd4a68ed700a926cafbed4dec691e19ad952d054b58ee462d467`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:32:02 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 20:32:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 20:32:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:32:08 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:32:08 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:32:08 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:32:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:32:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bf00bbc3dfb229dd261e340cf51cd7ab2c521606bf33a31c0151957364fb66`  
		Last Modified: Sat, 27 Mar 2021 20:32:48 GMT  
		Size: 37.2 MB (37174360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e093880828ab1d78f8852129cd98780c9b79e7f1f029b830991e8469b145b21`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c239f527a9508c7200c46a24012866348a320a71d4df24fad6fea341f793e679`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:b906902169272e864f480f9086430f53c626dc49250202c66aa2d5fe4c7833cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104164159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7abeabbf2891b8bccfcf54b68a002c8132809ae3da54988d773b3013dffc2038`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:46 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 09:07:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:08:01 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:08:02 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:08:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:08:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a314e91b9ff7f5d05bb6d8035d6ca93b5cc938ae5339ce34e4c6206ae42995b`  
		Last Modified: Sat, 27 Mar 2021 09:08:48 GMT  
		Size: 34.7 MB (34738582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4220b10e3575373f9809be75ac373fd7d3ed227ed82a1a35a48482d78666fc`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664b33bbc1108e9b0e1dcb52fea68f46fd64ac4bdde359973d3a2782508b5ff3`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:96b61ed9e099f70d605ce003800ebfc6d795cae3bc1c8160513eb356b3a2dae8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104976110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0668ff37c1069274906f210e54abc661736c4a0a36f187bc6269e78f617e3d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:44:15 GMT
ADD file:cf753fedc426819aa5f93f4ad934479efd8fbf024b408627239b77ddc5223108 in / 
# Fri, 26 Mar 2021 15:44:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:21:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 23:47:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 23:47:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 23:47:41 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 23:47:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 23:47:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 23:47:48 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 23:47:48 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 23:47:49 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 23:47:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 23:47:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1a0736e738921f2c70c8ce48d5ba8b042279c41c41f32a1af43a6cbd299f6d89`  
		Last Modified: Fri, 26 Mar 2021 15:50:55 GMT  
		Size: 43.2 MB (43176405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c963a30dbe4f7f47cba7603121834cb6b6f206d9c25e8a96df41cfd42eab3e`  
		Last Modified: Sat, 27 Mar 2021 04:30:49 GMT  
		Size: 10.2 MB (10201048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97078da83c94ce9db743f96c02e8deaf24987dd4e94aced6c6b5ceb860b8f8ac`  
		Last Modified: Sat, 27 Mar 2021 04:30:47 GMT  
		Size: 4.1 MB (4096666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261e51104922fc98e8cfda60b3facdb439cab292dae4e0369fb8fffc0b1fd201`  
		Last Modified: Sat, 27 Mar 2021 23:48:05 GMT  
		Size: 13.0 MB (12968150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c744e842337b47b39ce131e84dd273e87f1ec810aa84a982428daefab495bb`  
		Last Modified: Sat, 27 Mar 2021 23:48:03 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f0fc49d8045dd78f0dd563618df408b7f15a87ac48807b4260c8e7a58a4cb`  
		Last Modified: Sat, 27 Mar 2021 23:48:23 GMT  
		Size: 34.5 MB (34530530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab540866ae425c35d3013643752b949d4c456be133d3b905c1e0ee34d652b1cc`  
		Last Modified: Sat, 27 Mar 2021 23:48:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a0a5263d418958b889d8c7bb185ecb018a71d0dee3309477db60c2f4a9888b`  
		Last Modified: Sat, 27 Mar 2021 23:48:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
