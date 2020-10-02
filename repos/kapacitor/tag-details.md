<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5.6`](#kapacitor156)
-	[`kapacitor:1.5.6-alpine`](#kapacitor156-alpine)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:809300107e6811bc3607f4d7f15821f0c15b6f07b1704fbfd3c8c38c8eb7b55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:965484c1239e6ffcfa98a7f7a8734acb799107b50288cc165a8e4cbf76580698
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96274519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0097883df13c92f8d1855fd47b1e7c7880f09d40926e37b63ad519027a07b874`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:22:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 11 Sep 2020 03:22:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:22:31 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 11 Sep 2020 03:22:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 11 Sep 2020 03:22:34 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 11 Sep 2020 03:22:34 GMT
EXPOSE 9092
# Fri, 11 Sep 2020 03:22:34 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 11 Sep 2020 03:22:34 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 11 Sep 2020 03:22:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:22:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2a4ffe01703531900ae63d26540ffde791eeeb9edef562a468cf78eeb25918`  
		Last Modified: Fri, 11 Sep 2020 03:23:02 GMT  
		Size: 13.1 MB (13118906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f150ed336d25bee7ef9195279541ae9412961943bc6e7f28ab26d291a7f47e`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13fbe87783267d96789fea92233f9d7abb0ab26cac84cc58db4de359eec8120`  
		Last Modified: Fri, 11 Sep 2020 03:23:06 GMT  
		Size: 22.7 MB (22694288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e14dfcd0832ecc983723530d0214f774e60b1d30c170f6143c8f662f2f7a4c2`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e0362a07b784456b10ee89dd81a2ec66a766bf6c07226d55227d03104d662e`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:947c098d03d2f73ca66c275cc0f2865b698ba75f66770d5583c975219f8b409c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90072332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060673199379204219e6789ac9d7ff201b902c4eba74f890f9e77c1083791711`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:13:17 GMT
ADD file:3da15ca153ab01cc777bb2a828e1097edc064f49012d96e9b0789cc4cbe9c205 in / 
# Thu, 10 Sep 2020 00:13:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:55:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:52:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:52:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:52:11 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 10 Sep 2020 22:52:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 10 Sep 2020 22:52:19 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:52:20 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:52:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:52:21 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:52:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:52:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2dc31d01bd52bc4550017dd5cb9e295a7998fbfa6b3ea3f612efb5da666b3600`  
		Last Modified: Thu, 10 Sep 2020 00:21:14 GMT  
		Size: 42.1 MB (42111430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f054c3bb715838c3b5b7a1b87d44bb27e66b730c6f46043718676fd2b5f82a9`  
		Last Modified: Thu, 10 Sep 2020 02:05:53 GMT  
		Size: 9.4 MB (9443974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7852e0ac40ce276d38d43909de6fc6e0283548a22510dba9ed39e9c093895f`  
		Last Modified: Thu, 10 Sep 2020 02:05:52 GMT  
		Size: 3.9 MB (3919884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75cf43b24edcf3677bb001f8f6712c6d3bb022a07985d07975c043341b1e85`  
		Last Modified: Thu, 10 Sep 2020 22:53:01 GMT  
		Size: 13.3 MB (13285643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574d27101ee6986e442ec28fabe44786b74e0483a20f8843d082ccb83e88f30f`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173b127de5165a30ee93761db8f2224973f8c7d2cf2d82a675111314b58d66bd`  
		Last Modified: Thu, 10 Sep 2020 22:53:08 GMT  
		Size: 21.3 MB (21308089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a16f3bead7188728d96b70209eb9dd3809d55c113391a2130819d966d529fa6`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d3ca923a3467b7eaa583e661952c6f3426db00b783de8d4d9a920008364f72`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:a6828f3eb4b8bef3c28c0adabce9d87c4d33df2e653c7672e09a67960a5d3101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91102336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7c1d1ae227c5d7e5fd57c681bdbfbd2eaebed966b7dae63af9723aaec00728`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:10:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:10:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:10:39 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 10 Sep 2020 22:10:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 10 Sep 2020 22:10:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:10:47 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:10:48 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:10:49 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:10:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:10:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22516f755571abeef68a3fb7443a74dbdc920a646146d537a19d039fbe830cc9`  
		Last Modified: Thu, 10 Sep 2020 22:11:26 GMT  
		Size: 12.8 MB (12823494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9439323c8548ace51650ae2fb17736a08ec0be37bb0126338e6ff56147ed5f`  
		Last Modified: Thu, 10 Sep 2020 22:11:23 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a806fbe8209ad6aa508fce353489741498eda5533e831e5d5f5eb312ec4de283`  
		Last Modified: Thu, 10 Sep 2020 22:11:32 GMT  
		Size: 21.3 MB (21307816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96776c0961c11b946d80e2f5de19012dc9e8fec9f1e63e3d3807af24e0b6d10c`  
		Last Modified: Thu, 10 Sep 2020 22:11:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e030054d7640b371e0c130c978036e23c8bcce7af0bf5f5075aa367968992c`  
		Last Modified: Thu, 10 Sep 2020 22:11:23 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:809300107e6811bc3607f4d7f15821f0c15b6f07b1704fbfd3c8c38c8eb7b55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:965484c1239e6ffcfa98a7f7a8734acb799107b50288cc165a8e4cbf76580698
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96274519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0097883df13c92f8d1855fd47b1e7c7880f09d40926e37b63ad519027a07b874`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:22:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 11 Sep 2020 03:22:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:22:31 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 11 Sep 2020 03:22:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 11 Sep 2020 03:22:34 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 11 Sep 2020 03:22:34 GMT
EXPOSE 9092
# Fri, 11 Sep 2020 03:22:34 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 11 Sep 2020 03:22:34 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 11 Sep 2020 03:22:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:22:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2a4ffe01703531900ae63d26540ffde791eeeb9edef562a468cf78eeb25918`  
		Last Modified: Fri, 11 Sep 2020 03:23:02 GMT  
		Size: 13.1 MB (13118906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f150ed336d25bee7ef9195279541ae9412961943bc6e7f28ab26d291a7f47e`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13fbe87783267d96789fea92233f9d7abb0ab26cac84cc58db4de359eec8120`  
		Last Modified: Fri, 11 Sep 2020 03:23:06 GMT  
		Size: 22.7 MB (22694288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e14dfcd0832ecc983723530d0214f774e60b1d30c170f6143c8f662f2f7a4c2`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e0362a07b784456b10ee89dd81a2ec66a766bf6c07226d55227d03104d662e`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:947c098d03d2f73ca66c275cc0f2865b698ba75f66770d5583c975219f8b409c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90072332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060673199379204219e6789ac9d7ff201b902c4eba74f890f9e77c1083791711`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:13:17 GMT
ADD file:3da15ca153ab01cc777bb2a828e1097edc064f49012d96e9b0789cc4cbe9c205 in / 
# Thu, 10 Sep 2020 00:13:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:55:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:52:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:52:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:52:11 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 10 Sep 2020 22:52:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 10 Sep 2020 22:52:19 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:52:20 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:52:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:52:21 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:52:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:52:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2dc31d01bd52bc4550017dd5cb9e295a7998fbfa6b3ea3f612efb5da666b3600`  
		Last Modified: Thu, 10 Sep 2020 00:21:14 GMT  
		Size: 42.1 MB (42111430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f054c3bb715838c3b5b7a1b87d44bb27e66b730c6f46043718676fd2b5f82a9`  
		Last Modified: Thu, 10 Sep 2020 02:05:53 GMT  
		Size: 9.4 MB (9443974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7852e0ac40ce276d38d43909de6fc6e0283548a22510dba9ed39e9c093895f`  
		Last Modified: Thu, 10 Sep 2020 02:05:52 GMT  
		Size: 3.9 MB (3919884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75cf43b24edcf3677bb001f8f6712c6d3bb022a07985d07975c043341b1e85`  
		Last Modified: Thu, 10 Sep 2020 22:53:01 GMT  
		Size: 13.3 MB (13285643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574d27101ee6986e442ec28fabe44786b74e0483a20f8843d082ccb83e88f30f`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173b127de5165a30ee93761db8f2224973f8c7d2cf2d82a675111314b58d66bd`  
		Last Modified: Thu, 10 Sep 2020 22:53:08 GMT  
		Size: 21.3 MB (21308089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a16f3bead7188728d96b70209eb9dd3809d55c113391a2130819d966d529fa6`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d3ca923a3467b7eaa583e661952c6f3426db00b783de8d4d9a920008364f72`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:a6828f3eb4b8bef3c28c0adabce9d87c4d33df2e653c7672e09a67960a5d3101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91102336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7c1d1ae227c5d7e5fd57c681bdbfbd2eaebed966b7dae63af9723aaec00728`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:10:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:10:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:10:39 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 10 Sep 2020 22:10:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 10 Sep 2020 22:10:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:10:47 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:10:48 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:10:49 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:10:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:10:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22516f755571abeef68a3fb7443a74dbdc920a646146d537a19d039fbe830cc9`  
		Last Modified: Thu, 10 Sep 2020 22:11:26 GMT  
		Size: 12.8 MB (12823494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9439323c8548ace51650ae2fb17736a08ec0be37bb0126338e6ff56147ed5f`  
		Last Modified: Thu, 10 Sep 2020 22:11:23 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a806fbe8209ad6aa508fce353489741498eda5533e831e5d5f5eb312ec4de283`  
		Last Modified: Thu, 10 Sep 2020 22:11:32 GMT  
		Size: 21.3 MB (21307816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96776c0961c11b946d80e2f5de19012dc9e8fec9f1e63e3d3807af24e0b6d10c`  
		Last Modified: Thu, 10 Sep 2020 22:11:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e030054d7640b371e0c130c978036e23c8bcce7af0bf5f5075aa367968992c`  
		Last Modified: Thu, 10 Sep 2020 22:11:23 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:708aa7a25f5d1d6e7feb3f0617bb5aada0ad6f70fa0f35b2439f056864931762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:6c56395b2767b13e4badc4cff8c58cd93e22e0aaeaf1abcd9ed3dcd4246b9caf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19677542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac1c89cbe21ec99362921876624cb874b08322c1d84a951ba836ca3752b693f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:39 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 02 Sep 2020 00:16:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:16:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 00:16:31 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 00:16:31 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 00:16:31 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 02 Sep 2020 00:16:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:16:31 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac836c5a581fe484d430996440a28eecf37316376ba156f051bf920ababfc37`  
		Last Modified: Wed, 02 Sep 2020 00:17:06 GMT  
		Size: 16.6 MB (16598563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77b99c5ea852abc105448a587360b853163d8fcdcd39d44c6d94a729a59ede1`  
		Last Modified: Wed, 02 Sep 2020 00:17:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2bf5aaf0c284238e874e05bf476763b565f10d432d8d47f7b9f3793369ba0`  
		Last Modified: Wed, 02 Sep 2020 00:17:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:708aa7a25f5d1d6e7feb3f0617bb5aada0ad6f70fa0f35b2439f056864931762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:6c56395b2767b13e4badc4cff8c58cd93e22e0aaeaf1abcd9ed3dcd4246b9caf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19677542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac1c89cbe21ec99362921876624cb874b08322c1d84a951ba836ca3752b693f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:39 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 02 Sep 2020 00:16:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:16:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 00:16:31 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 00:16:31 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 00:16:31 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 02 Sep 2020 00:16:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:16:31 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac836c5a581fe484d430996440a28eecf37316376ba156f051bf920ababfc37`  
		Last Modified: Wed, 02 Sep 2020 00:17:06 GMT  
		Size: 16.6 MB (16598563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77b99c5ea852abc105448a587360b853163d8fcdcd39d44c6d94a729a59ede1`  
		Last Modified: Wed, 02 Sep 2020 00:17:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2bf5aaf0c284238e874e05bf476763b565f10d432d8d47f7b9f3793369ba0`  
		Last Modified: Wed, 02 Sep 2020 00:17:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:65c5596ef7aacf0a024c25f7edb9e1b32011215d8365f27d4510f9e8721e2935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:eead9b379e0bb9b7dbcccf95e8daba5fe18e4a5a141eead7045f056e3cbffeae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109993688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5337570e18a4eb3ebcc71f5465d88cf65721dd431b8332a8feae133eaccaa852`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:22:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 11 Sep 2020 03:22:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:22:42 GMT
ENV KAPACITOR_VERSION=1.5.6
# Fri, 11 Sep 2020 03:22:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 11 Sep 2020 03:22:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 11 Sep 2020 03:22:46 GMT
EXPOSE 9092
# Fri, 11 Sep 2020 03:22:46 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 11 Sep 2020 03:22:46 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 11 Sep 2020 03:22:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:22:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2a4ffe01703531900ae63d26540ffde791eeeb9edef562a468cf78eeb25918`  
		Last Modified: Fri, 11 Sep 2020 03:23:02 GMT  
		Size: 13.1 MB (13118906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f150ed336d25bee7ef9195279541ae9412961943bc6e7f28ab26d291a7f47e`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971831a9009572a8aabc2fd127df982b4d9f564a2cc30b3b5719d0a97f4c0e4d`  
		Last Modified: Fri, 11 Sep 2020 03:23:15 GMT  
		Size: 36.4 MB (36413458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8bd252b2b84983bc6f60677cb87e756d6c7918424c366c653538c9bfc346c9`  
		Last Modified: Fri, 11 Sep 2020 03:23:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8c717fbb9e3e9488ecabc5418c15a17acfd9a7c44db5efcb2f247c71ba71a`  
		Last Modified: Fri, 11 Sep 2020 03:23:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:6f96969e5640da27a9099814df57a373f39a489f0307baeae38bc83215860772
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102905039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccc138a73017badc1dafbc7db36956cd2f257674020a91be3416774b52a93ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:13:17 GMT
ADD file:3da15ca153ab01cc777bb2a828e1097edc064f49012d96e9b0789cc4cbe9c205 in / 
# Thu, 10 Sep 2020 00:13:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:55:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:52:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:52:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:52:34 GMT
ENV KAPACITOR_VERSION=1.5.6
# Thu, 10 Sep 2020 22:52:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 10 Sep 2020 22:52:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:52:43 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:52:44 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:52:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:52:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:52:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2dc31d01bd52bc4550017dd5cb9e295a7998fbfa6b3ea3f612efb5da666b3600`  
		Last Modified: Thu, 10 Sep 2020 00:21:14 GMT  
		Size: 42.1 MB (42111430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f054c3bb715838c3b5b7a1b87d44bb27e66b730c6f46043718676fd2b5f82a9`  
		Last Modified: Thu, 10 Sep 2020 02:05:53 GMT  
		Size: 9.4 MB (9443974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7852e0ac40ce276d38d43909de6fc6e0283548a22510dba9ed39e9c093895f`  
		Last Modified: Thu, 10 Sep 2020 02:05:52 GMT  
		Size: 3.9 MB (3919884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75cf43b24edcf3677bb001f8f6712c6d3bb022a07985d07975c043341b1e85`  
		Last Modified: Thu, 10 Sep 2020 22:53:01 GMT  
		Size: 13.3 MB (13285643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574d27101ee6986e442ec28fabe44786b74e0483a20f8843d082ccb83e88f30f`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3525b18c34520931d2ef62cd55424b6f02beb7f5de39c0f0f723112f349c30`  
		Last Modified: Thu, 10 Sep 2020 22:53:25 GMT  
		Size: 34.1 MB (34140796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1e4d39bce2f6964424640cd5367a9e12887c160699bf9d5d2fd628bec85af2`  
		Last Modified: Thu, 10 Sep 2020 22:53:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41931ff6aa8b929f680ff158a6307c2edb2f91e2c312e764966432891a694b5`  
		Last Modified: Thu, 10 Sep 2020 22:53:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:008fac5720dca73b0f694a75f8908a2558b152e709a872546b0fe7b817ff9e00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103707279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dfff79a8ccab1b685dadf209845ac003c5a8c8e442e835ecb3dc9521148404`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:10:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:10:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:11:00 GMT
ENV KAPACITOR_VERSION=1.5.6
# Thu, 10 Sep 2020 22:11:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 10 Sep 2020 22:11:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:11:08 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:11:09 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:11:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:11:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:11:11 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22516f755571abeef68a3fb7443a74dbdc920a646146d537a19d039fbe830cc9`  
		Last Modified: Thu, 10 Sep 2020 22:11:26 GMT  
		Size: 12.8 MB (12823494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9439323c8548ace51650ae2fb17736a08ec0be37bb0126338e6ff56147ed5f`  
		Last Modified: Thu, 10 Sep 2020 22:11:23 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87328495ff8fed6ae5ad77111ca5ff805bdc871f4e555df953de136a6d00050`  
		Last Modified: Thu, 10 Sep 2020 22:11:48 GMT  
		Size: 33.9 MB (33912757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d44b1e84a03a27d6f6b494b5f7dec4505d8f389eda17a47a7a7d1a5fc30705`  
		Last Modified: Thu, 10 Sep 2020 22:11:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdaaf0d42a7b9c1f5d5b4f8b8c130d900daf095f982e208e1883671a4009bab`  
		Last Modified: Thu, 10 Sep 2020 22:11:40 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.6`

```console
$ docker pull kapacitor@sha256:65c5596ef7aacf0a024c25f7edb9e1b32011215d8365f27d4510f9e8721e2935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:eead9b379e0bb9b7dbcccf95e8daba5fe18e4a5a141eead7045f056e3cbffeae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109993688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5337570e18a4eb3ebcc71f5465d88cf65721dd431b8332a8feae133eaccaa852`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:22:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 11 Sep 2020 03:22:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:22:42 GMT
ENV KAPACITOR_VERSION=1.5.6
# Fri, 11 Sep 2020 03:22:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 11 Sep 2020 03:22:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 11 Sep 2020 03:22:46 GMT
EXPOSE 9092
# Fri, 11 Sep 2020 03:22:46 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 11 Sep 2020 03:22:46 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 11 Sep 2020 03:22:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:22:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2a4ffe01703531900ae63d26540ffde791eeeb9edef562a468cf78eeb25918`  
		Last Modified: Fri, 11 Sep 2020 03:23:02 GMT  
		Size: 13.1 MB (13118906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f150ed336d25bee7ef9195279541ae9412961943bc6e7f28ab26d291a7f47e`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971831a9009572a8aabc2fd127df982b4d9f564a2cc30b3b5719d0a97f4c0e4d`  
		Last Modified: Fri, 11 Sep 2020 03:23:15 GMT  
		Size: 36.4 MB (36413458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8bd252b2b84983bc6f60677cb87e756d6c7918424c366c653538c9bfc346c9`  
		Last Modified: Fri, 11 Sep 2020 03:23:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8c717fbb9e3e9488ecabc5418c15a17acfd9a7c44db5efcb2f247c71ba71a`  
		Last Modified: Fri, 11 Sep 2020 03:23:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.6` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:6f96969e5640da27a9099814df57a373f39a489f0307baeae38bc83215860772
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102905039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccc138a73017badc1dafbc7db36956cd2f257674020a91be3416774b52a93ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:13:17 GMT
ADD file:3da15ca153ab01cc777bb2a828e1097edc064f49012d96e9b0789cc4cbe9c205 in / 
# Thu, 10 Sep 2020 00:13:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:55:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:52:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:52:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:52:34 GMT
ENV KAPACITOR_VERSION=1.5.6
# Thu, 10 Sep 2020 22:52:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 10 Sep 2020 22:52:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:52:43 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:52:44 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:52:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:52:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:52:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2dc31d01bd52bc4550017dd5cb9e295a7998fbfa6b3ea3f612efb5da666b3600`  
		Last Modified: Thu, 10 Sep 2020 00:21:14 GMT  
		Size: 42.1 MB (42111430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f054c3bb715838c3b5b7a1b87d44bb27e66b730c6f46043718676fd2b5f82a9`  
		Last Modified: Thu, 10 Sep 2020 02:05:53 GMT  
		Size: 9.4 MB (9443974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7852e0ac40ce276d38d43909de6fc6e0283548a22510dba9ed39e9c093895f`  
		Last Modified: Thu, 10 Sep 2020 02:05:52 GMT  
		Size: 3.9 MB (3919884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75cf43b24edcf3677bb001f8f6712c6d3bb022a07985d07975c043341b1e85`  
		Last Modified: Thu, 10 Sep 2020 22:53:01 GMT  
		Size: 13.3 MB (13285643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574d27101ee6986e442ec28fabe44786b74e0483a20f8843d082ccb83e88f30f`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3525b18c34520931d2ef62cd55424b6f02beb7f5de39c0f0f723112f349c30`  
		Last Modified: Thu, 10 Sep 2020 22:53:25 GMT  
		Size: 34.1 MB (34140796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1e4d39bce2f6964424640cd5367a9e12887c160699bf9d5d2fd628bec85af2`  
		Last Modified: Thu, 10 Sep 2020 22:53:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41931ff6aa8b929f680ff158a6307c2edb2f91e2c312e764966432891a694b5`  
		Last Modified: Thu, 10 Sep 2020 22:53:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:008fac5720dca73b0f694a75f8908a2558b152e709a872546b0fe7b817ff9e00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103707279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dfff79a8ccab1b685dadf209845ac003c5a8c8e442e835ecb3dc9521148404`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:10:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:10:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:11:00 GMT
ENV KAPACITOR_VERSION=1.5.6
# Thu, 10 Sep 2020 22:11:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 10 Sep 2020 22:11:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:11:08 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:11:09 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:11:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:11:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:11:11 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22516f755571abeef68a3fb7443a74dbdc920a646146d537a19d039fbe830cc9`  
		Last Modified: Thu, 10 Sep 2020 22:11:26 GMT  
		Size: 12.8 MB (12823494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9439323c8548ace51650ae2fb17736a08ec0be37bb0126338e6ff56147ed5f`  
		Last Modified: Thu, 10 Sep 2020 22:11:23 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87328495ff8fed6ae5ad77111ca5ff805bdc871f4e555df953de136a6d00050`  
		Last Modified: Thu, 10 Sep 2020 22:11:48 GMT  
		Size: 33.9 MB (33912757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d44b1e84a03a27d6f6b494b5f7dec4505d8f389eda17a47a7a7d1a5fc30705`  
		Last Modified: Thu, 10 Sep 2020 22:11:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdaaf0d42a7b9c1f5d5b4f8b8c130d900daf095f982e208e1883671a4009bab`  
		Last Modified: Thu, 10 Sep 2020 22:11:40 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.6-alpine`

```console
$ docker pull kapacitor@sha256:601c43fa03415b10bad3b140984ea8f458bba0fd3d34db4413004626ab7a533a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:ec7badc3d2b9660fbb8362d560e590a5a11536da60414356ba370f7da214ed24
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23148286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccdbf941acbff8fdeeb125726f579391ab3eac90b1e442276e625b7c792e3cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:56 GMT
ENV KAPACITOR_VERSION=1.5.6
# Fri, 02 Oct 2020 01:39:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:39:13 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Oct 2020 01:39:13 GMT
EXPOSE 9092
# Fri, 02 Oct 2020 01:39:14 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Oct 2020 01:39:14 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 02 Oct 2020 01:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:39:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a8d572845cce717fde5f35ff512fd54a4a7d57858a0533316976c150fa154e`  
		Last Modified: Fri, 02 Oct 2020 01:39:41 GMT  
		Size: 20.1 MB (20069308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f943370a3f0984909fe0a602c1b91554241d00810b19d4dc2bf4ea8a79d832b`  
		Last Modified: Fri, 02 Oct 2020 01:39:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e82ea3c666b1fa565cb994b107c6d1fe53d6f36258ae08ac40b48beef2fc7d8`  
		Last Modified: Fri, 02 Oct 2020 01:39:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:601c43fa03415b10bad3b140984ea8f458bba0fd3d34db4413004626ab7a533a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:ec7badc3d2b9660fbb8362d560e590a5a11536da60414356ba370f7da214ed24
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23148286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccdbf941acbff8fdeeb125726f579391ab3eac90b1e442276e625b7c792e3cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:56 GMT
ENV KAPACITOR_VERSION=1.5.6
# Fri, 02 Oct 2020 01:39:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:39:13 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Oct 2020 01:39:13 GMT
EXPOSE 9092
# Fri, 02 Oct 2020 01:39:14 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Oct 2020 01:39:14 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 02 Oct 2020 01:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:39:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a8d572845cce717fde5f35ff512fd54a4a7d57858a0533316976c150fa154e`  
		Last Modified: Fri, 02 Oct 2020 01:39:41 GMT  
		Size: 20.1 MB (20069308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f943370a3f0984909fe0a602c1b91554241d00810b19d4dc2bf4ea8a79d832b`  
		Last Modified: Fri, 02 Oct 2020 01:39:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e82ea3c666b1fa565cb994b107c6d1fe53d6f36258ae08ac40b48beef2fc7d8`  
		Last Modified: Fri, 02 Oct 2020 01:39:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:601c43fa03415b10bad3b140984ea8f458bba0fd3d34db4413004626ab7a533a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:ec7badc3d2b9660fbb8362d560e590a5a11536da60414356ba370f7da214ed24
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23148286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccdbf941acbff8fdeeb125726f579391ab3eac90b1e442276e625b7c792e3cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:56 GMT
ENV KAPACITOR_VERSION=1.5.6
# Fri, 02 Oct 2020 01:39:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:39:13 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Oct 2020 01:39:13 GMT
EXPOSE 9092
# Fri, 02 Oct 2020 01:39:14 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Oct 2020 01:39:14 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 02 Oct 2020 01:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:39:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a8d572845cce717fde5f35ff512fd54a4a7d57858a0533316976c150fa154e`  
		Last Modified: Fri, 02 Oct 2020 01:39:41 GMT  
		Size: 20.1 MB (20069308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f943370a3f0984909fe0a602c1b91554241d00810b19d4dc2bf4ea8a79d832b`  
		Last Modified: Fri, 02 Oct 2020 01:39:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e82ea3c666b1fa565cb994b107c6d1fe53d6f36258ae08ac40b48beef2fc7d8`  
		Last Modified: Fri, 02 Oct 2020 01:39:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:65c5596ef7aacf0a024c25f7edb9e1b32011215d8365f27d4510f9e8721e2935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:eead9b379e0bb9b7dbcccf95e8daba5fe18e4a5a141eead7045f056e3cbffeae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109993688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5337570e18a4eb3ebcc71f5465d88cf65721dd431b8332a8feae133eaccaa852`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:22:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 11 Sep 2020 03:22:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:22:42 GMT
ENV KAPACITOR_VERSION=1.5.6
# Fri, 11 Sep 2020 03:22:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 11 Sep 2020 03:22:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 11 Sep 2020 03:22:46 GMT
EXPOSE 9092
# Fri, 11 Sep 2020 03:22:46 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 11 Sep 2020 03:22:46 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 11 Sep 2020 03:22:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:22:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2a4ffe01703531900ae63d26540ffde791eeeb9edef562a468cf78eeb25918`  
		Last Modified: Fri, 11 Sep 2020 03:23:02 GMT  
		Size: 13.1 MB (13118906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f150ed336d25bee7ef9195279541ae9412961943bc6e7f28ab26d291a7f47e`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971831a9009572a8aabc2fd127df982b4d9f564a2cc30b3b5719d0a97f4c0e4d`  
		Last Modified: Fri, 11 Sep 2020 03:23:15 GMT  
		Size: 36.4 MB (36413458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8bd252b2b84983bc6f60677cb87e756d6c7918424c366c653538c9bfc346c9`  
		Last Modified: Fri, 11 Sep 2020 03:23:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8c717fbb9e3e9488ecabc5418c15a17acfd9a7c44db5efcb2f247c71ba71a`  
		Last Modified: Fri, 11 Sep 2020 03:23:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:6f96969e5640da27a9099814df57a373f39a489f0307baeae38bc83215860772
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102905039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccc138a73017badc1dafbc7db36956cd2f257674020a91be3416774b52a93ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:13:17 GMT
ADD file:3da15ca153ab01cc777bb2a828e1097edc064f49012d96e9b0789cc4cbe9c205 in / 
# Thu, 10 Sep 2020 00:13:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:55:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:52:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:52:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:52:34 GMT
ENV KAPACITOR_VERSION=1.5.6
# Thu, 10 Sep 2020 22:52:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 10 Sep 2020 22:52:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:52:43 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:52:44 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:52:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:52:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:52:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2dc31d01bd52bc4550017dd5cb9e295a7998fbfa6b3ea3f612efb5da666b3600`  
		Last Modified: Thu, 10 Sep 2020 00:21:14 GMT  
		Size: 42.1 MB (42111430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f054c3bb715838c3b5b7a1b87d44bb27e66b730c6f46043718676fd2b5f82a9`  
		Last Modified: Thu, 10 Sep 2020 02:05:53 GMT  
		Size: 9.4 MB (9443974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7852e0ac40ce276d38d43909de6fc6e0283548a22510dba9ed39e9c093895f`  
		Last Modified: Thu, 10 Sep 2020 02:05:52 GMT  
		Size: 3.9 MB (3919884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75cf43b24edcf3677bb001f8f6712c6d3bb022a07985d07975c043341b1e85`  
		Last Modified: Thu, 10 Sep 2020 22:53:01 GMT  
		Size: 13.3 MB (13285643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574d27101ee6986e442ec28fabe44786b74e0483a20f8843d082ccb83e88f30f`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3525b18c34520931d2ef62cd55424b6f02beb7f5de39c0f0f723112f349c30`  
		Last Modified: Thu, 10 Sep 2020 22:53:25 GMT  
		Size: 34.1 MB (34140796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1e4d39bce2f6964424640cd5367a9e12887c160699bf9d5d2fd628bec85af2`  
		Last Modified: Thu, 10 Sep 2020 22:53:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41931ff6aa8b929f680ff158a6307c2edb2f91e2c312e764966432891a694b5`  
		Last Modified: Thu, 10 Sep 2020 22:53:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:008fac5720dca73b0f694a75f8908a2558b152e709a872546b0fe7b817ff9e00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103707279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dfff79a8ccab1b685dadf209845ac003c5a8c8e442e835ecb3dc9521148404`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:10:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:10:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:11:00 GMT
ENV KAPACITOR_VERSION=1.5.6
# Thu, 10 Sep 2020 22:11:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 10 Sep 2020 22:11:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:11:08 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:11:09 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:11:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:11:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:11:11 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22516f755571abeef68a3fb7443a74dbdc920a646146d537a19d039fbe830cc9`  
		Last Modified: Thu, 10 Sep 2020 22:11:26 GMT  
		Size: 12.8 MB (12823494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9439323c8548ace51650ae2fb17736a08ec0be37bb0126338e6ff56147ed5f`  
		Last Modified: Thu, 10 Sep 2020 22:11:23 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87328495ff8fed6ae5ad77111ca5ff805bdc871f4e555df953de136a6d00050`  
		Last Modified: Thu, 10 Sep 2020 22:11:48 GMT  
		Size: 33.9 MB (33912757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d44b1e84a03a27d6f6b494b5f7dec4505d8f389eda17a47a7a7d1a5fc30705`  
		Last Modified: Thu, 10 Sep 2020 22:11:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdaaf0d42a7b9c1f5d5b4f8b8c130d900daf095f982e208e1883671a4009bab`  
		Last Modified: Thu, 10 Sep 2020 22:11:40 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
