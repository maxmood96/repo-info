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
$ docker pull kapacitor@sha256:8dd74ba84dfc0576b340f774ec7e9085e945e6efd8b10d21b31354c6f589ba48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:b053a9acd2c0517976a968ad2ad8d32d6d923485a2f08d978e7fbd4d9cdd4405
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96312876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd37e8545fee1e717a189f28253ac54b925cd00b4deffc6e8acff68efe9583`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:43:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:43:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 May 2020 09:44:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 16 May 2020 09:44:18 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 16 May 2020 09:44:18 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 16 May 2020 09:44:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 16 May 2020 09:44:22 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 May 2020 09:44:22 GMT
EXPOSE 9092
# Sat, 16 May 2020 09:44:22 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 May 2020 09:44:23 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 16 May 2020 09:44:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 May 2020 09:44:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b194b0e3c928807cfabf081055a117585ba5bf6697f65b2fede02225a5d73ad2`  
		Last Modified: Fri, 15 May 2020 17:55:27 GMT  
		Size: 10.8 MB (10797475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ec00f35d5b2d1db6b8e925a3005c1a285365775028db0339903ddaeec4763`  
		Last Modified: Fri, 15 May 2020 17:55:29 GMT  
		Size: 4.3 MB (4340139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384f0606b9fbbbd98395f99922e252f11cfa34e5a6630c12b5f0487f7f17011`  
		Last Modified: Sat, 16 May 2020 09:44:50 GMT  
		Size: 13.1 MB (13102550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12c2bdba4f53fc9ba35acf2ec0682e9c71eabd9e0ea0f1e02e575885c572d2f`  
		Last Modified: Sat, 16 May 2020 09:44:48 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604e999c809dd29a15a05b380ff888ce5d8f2f4e59d91dfd050a3b24ff298fe2`  
		Last Modified: Sat, 16 May 2020 09:44:54 GMT  
		Size: 22.7 MB (22694274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3cafb0bf044554bd54be0f8981c8e86298c073d30e66351d812cb533cf724c`  
		Last Modified: Sat, 16 May 2020 09:44:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306e48e47a264276ae324de2ff43768409fed2ec821ab689a45b357565f045d1`  
		Last Modified: Sat, 16 May 2020 09:44:49 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:8f38b7b7a9389c3c1a32a7bc445ab224dc0cb09968fa248472b62cdb8a60de14
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90056836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667a359e8ed7fbb9ae00d26cd700056d2607bdca209ef9d138ca44be91bff37f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:07 GMT
ADD file:c0b9ed1244ec0acfc9054c7cb80c768878e3da99740f981ba3a82bdd854305db in / 
# Tue, 09 Jun 2020 01:06:09 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:02:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:02:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:12:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:12:27 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:12:28 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 09 Jun 2020 21:12:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 09 Jun 2020 21:12:36 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:12:36 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:12:37 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:12:38 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:12:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:12:39 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2566ca784846d2d0d4f9105084d94d68d8ea1a82a06a76c5bcd991ce5a10cda1`  
		Last Modified: Tue, 09 Jun 2020 01:13:35 GMT  
		Size: 42.1 MB (42102504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f976b5a12722f5e6e115157695654d36452b713c7fa64a860f8c9e14859402`  
		Last Modified: Tue, 09 Jun 2020 02:15:15 GMT  
		Size: 9.4 MB (9443335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35142ef6ea6c722cd0397799ab151e5da354eabc784b3acef29def7fa34e9bc`  
		Last Modified: Tue, 09 Jun 2020 02:15:13 GMT  
		Size: 3.9 MB (3918433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746389951d399e64371b3fed79516bd9416316ccb7e0a6cbfa8a9e08e546dacb`  
		Last Modified: Tue, 09 Jun 2020 21:13:14 GMT  
		Size: 13.3 MB (13281228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871c5b3b4857aae8365c881c8544b09dd2934c439a97a93284f6a5a47a36bb0`  
		Last Modified: Tue, 09 Jun 2020 21:13:12 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032696c59681727a5873cd8be04d9884313526b11d54ae19ecc027c02b33dbc1`  
		Last Modified: Tue, 09 Jun 2020 21:13:20 GMT  
		Size: 21.3 MB (21308074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecae795136bf9393070dfa989d8080601a3a49370be3f3870b66ec4caac485ef`  
		Last Modified: Tue, 09 Jun 2020 21:13:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9dec00ddc260973531b927762d98466ec8234b1354f5ba67b93a8a5442c795`  
		Last Modified: Tue, 09 Jun 2020 21:13:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:f4367dc9018be3a866f09910650a20869248793f1ed6b84725ada19d7727d689
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91086045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4efb15862a3eaf6153e0ca06962c16e5cc405d9a1cd29081689cfa5e40332b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:53:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:53:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:53:22 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 09 Jun 2020 21:53:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 09 Jun 2020 21:53:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:53:31 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:53:32 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:53:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:53:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:53:36 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0990c417a21ef9e268cc0822cd23968c4b17cded8170cce0c4d8f7e020e6fd`  
		Last Modified: Tue, 09 Jun 2020 02:50:17 GMT  
		Size: 9.7 MB (9699635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6b83fd41426d182f67fdac882a6bfcd3aad22d7226a653ae58d3046bd46b5e`  
		Last Modified: Tue, 09 Jun 2020 02:50:15 GMT  
		Size: 4.1 MB (4094104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba4c6acba469b82e3b6632aaecd1c975cfdad5cd4bd72880d93d97b0eff4282`  
		Last Modified: Tue, 09 Jun 2020 21:54:20 GMT  
		Size: 12.8 MB (12820241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fa9a95920831056c7d3dfc1b43b1c057680d0e4d91c5b72513f527a8ebb2f5`  
		Last Modified: Tue, 09 Jun 2020 21:54:19 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80321785b39311874ba39d5d67fba4cb2c6ab641254938dce85356fa733d2759`  
		Last Modified: Tue, 09 Jun 2020 21:54:24 GMT  
		Size: 21.3 MB (21307882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b1ff9000080e41276a2d6a96ca83f16a773b7c74e139980cd7a4c32330bb0`  
		Last Modified: Tue, 09 Jun 2020 21:54:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20d2c5383ef0d778d576096c143bc4bc18b62988d1197511bbc0d48308b2598`  
		Last Modified: Tue, 09 Jun 2020 21:54:19 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:8dd74ba84dfc0576b340f774ec7e9085e945e6efd8b10d21b31354c6f589ba48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:b053a9acd2c0517976a968ad2ad8d32d6d923485a2f08d978e7fbd4d9cdd4405
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96312876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd37e8545fee1e717a189f28253ac54b925cd00b4deffc6e8acff68efe9583`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:43:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:43:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 May 2020 09:44:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 16 May 2020 09:44:18 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 16 May 2020 09:44:18 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 16 May 2020 09:44:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 16 May 2020 09:44:22 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 May 2020 09:44:22 GMT
EXPOSE 9092
# Sat, 16 May 2020 09:44:22 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 May 2020 09:44:23 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 16 May 2020 09:44:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 May 2020 09:44:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b194b0e3c928807cfabf081055a117585ba5bf6697f65b2fede02225a5d73ad2`  
		Last Modified: Fri, 15 May 2020 17:55:27 GMT  
		Size: 10.8 MB (10797475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ec00f35d5b2d1db6b8e925a3005c1a285365775028db0339903ddaeec4763`  
		Last Modified: Fri, 15 May 2020 17:55:29 GMT  
		Size: 4.3 MB (4340139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384f0606b9fbbbd98395f99922e252f11cfa34e5a6630c12b5f0487f7f17011`  
		Last Modified: Sat, 16 May 2020 09:44:50 GMT  
		Size: 13.1 MB (13102550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12c2bdba4f53fc9ba35acf2ec0682e9c71eabd9e0ea0f1e02e575885c572d2f`  
		Last Modified: Sat, 16 May 2020 09:44:48 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604e999c809dd29a15a05b380ff888ce5d8f2f4e59d91dfd050a3b24ff298fe2`  
		Last Modified: Sat, 16 May 2020 09:44:54 GMT  
		Size: 22.7 MB (22694274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3cafb0bf044554bd54be0f8981c8e86298c073d30e66351d812cb533cf724c`  
		Last Modified: Sat, 16 May 2020 09:44:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306e48e47a264276ae324de2ff43768409fed2ec821ab689a45b357565f045d1`  
		Last Modified: Sat, 16 May 2020 09:44:49 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:8f38b7b7a9389c3c1a32a7bc445ab224dc0cb09968fa248472b62cdb8a60de14
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90056836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667a359e8ed7fbb9ae00d26cd700056d2607bdca209ef9d138ca44be91bff37f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:07 GMT
ADD file:c0b9ed1244ec0acfc9054c7cb80c768878e3da99740f981ba3a82bdd854305db in / 
# Tue, 09 Jun 2020 01:06:09 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:02:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:02:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:12:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:12:27 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:12:28 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 09 Jun 2020 21:12:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 09 Jun 2020 21:12:36 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:12:36 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:12:37 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:12:38 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:12:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:12:39 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2566ca784846d2d0d4f9105084d94d68d8ea1a82a06a76c5bcd991ce5a10cda1`  
		Last Modified: Tue, 09 Jun 2020 01:13:35 GMT  
		Size: 42.1 MB (42102504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f976b5a12722f5e6e115157695654d36452b713c7fa64a860f8c9e14859402`  
		Last Modified: Tue, 09 Jun 2020 02:15:15 GMT  
		Size: 9.4 MB (9443335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35142ef6ea6c722cd0397799ab151e5da354eabc784b3acef29def7fa34e9bc`  
		Last Modified: Tue, 09 Jun 2020 02:15:13 GMT  
		Size: 3.9 MB (3918433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746389951d399e64371b3fed79516bd9416316ccb7e0a6cbfa8a9e08e546dacb`  
		Last Modified: Tue, 09 Jun 2020 21:13:14 GMT  
		Size: 13.3 MB (13281228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871c5b3b4857aae8365c881c8544b09dd2934c439a97a93284f6a5a47a36bb0`  
		Last Modified: Tue, 09 Jun 2020 21:13:12 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032696c59681727a5873cd8be04d9884313526b11d54ae19ecc027c02b33dbc1`  
		Last Modified: Tue, 09 Jun 2020 21:13:20 GMT  
		Size: 21.3 MB (21308074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecae795136bf9393070dfa989d8080601a3a49370be3f3870b66ec4caac485ef`  
		Last Modified: Tue, 09 Jun 2020 21:13:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9dec00ddc260973531b927762d98466ec8234b1354f5ba67b93a8a5442c795`  
		Last Modified: Tue, 09 Jun 2020 21:13:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:f4367dc9018be3a866f09910650a20869248793f1ed6b84725ada19d7727d689
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91086045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4efb15862a3eaf6153e0ca06962c16e5cc405d9a1cd29081689cfa5e40332b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:53:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:53:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:53:22 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 09 Jun 2020 21:53:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 09 Jun 2020 21:53:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:53:31 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:53:32 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:53:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:53:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:53:36 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0990c417a21ef9e268cc0822cd23968c4b17cded8170cce0c4d8f7e020e6fd`  
		Last Modified: Tue, 09 Jun 2020 02:50:17 GMT  
		Size: 9.7 MB (9699635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6b83fd41426d182f67fdac882a6bfcd3aad22d7226a653ae58d3046bd46b5e`  
		Last Modified: Tue, 09 Jun 2020 02:50:15 GMT  
		Size: 4.1 MB (4094104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba4c6acba469b82e3b6632aaecd1c975cfdad5cd4bd72880d93d97b0eff4282`  
		Last Modified: Tue, 09 Jun 2020 21:54:20 GMT  
		Size: 12.8 MB (12820241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fa9a95920831056c7d3dfc1b43b1c057680d0e4d91c5b72513f527a8ebb2f5`  
		Last Modified: Tue, 09 Jun 2020 21:54:19 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80321785b39311874ba39d5d67fba4cb2c6ab641254938dce85356fa733d2759`  
		Last Modified: Tue, 09 Jun 2020 21:54:24 GMT  
		Size: 21.3 MB (21307882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b1ff9000080e41276a2d6a96ca83f16a773b7c74e139980cd7a4c32330bb0`  
		Last Modified: Tue, 09 Jun 2020 21:54:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20d2c5383ef0d778d576096c143bc4bc18b62988d1197511bbc0d48308b2598`  
		Last Modified: Tue, 09 Jun 2020 21:54:19 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:8b0f86288ce5e80c0945fbb24a5f5d7aa5129fb48c6623697613113ba262c26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c7b1106644920eb2f651cfad13d77f603d62ffaf2aeab6876104da4827f36199
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19673755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6c8025603ebb4b75bfe5509147b8534d99582e3964158ca0ba0046f2b8bae4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 14:41:51 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 24 Apr 2020 14:41:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Apr 2020 14:41:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 24 Apr 2020 14:41:56 GMT
EXPOSE 9092
# Fri, 24 Apr 2020 14:41:56 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 24 Apr 2020 14:41:56 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 24 Apr 2020 14:41:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 14:41:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85169d009bd5f0c0ab3d615ff03bc83196402a467630fd52b525956c374af54`  
		Last Modified: Fri, 24 Apr 2020 14:42:25 GMT  
		Size: 16.6 MB (16598643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255366c4ce6923eee6adadbec2d9183c32883ccbb872f78f55012ca66353ef28`  
		Last Modified: Fri, 24 Apr 2020 14:42:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0fb6e436ba41bf7cfedcc84ac2aa94b71cf21e4a8bdea8a172cc1d441dd954`  
		Last Modified: Fri, 24 Apr 2020 14:42:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:8b0f86288ce5e80c0945fbb24a5f5d7aa5129fb48c6623697613113ba262c26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c7b1106644920eb2f651cfad13d77f603d62ffaf2aeab6876104da4827f36199
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19673755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6c8025603ebb4b75bfe5509147b8534d99582e3964158ca0ba0046f2b8bae4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 14:41:51 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 24 Apr 2020 14:41:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Apr 2020 14:41:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 24 Apr 2020 14:41:56 GMT
EXPOSE 9092
# Fri, 24 Apr 2020 14:41:56 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 24 Apr 2020 14:41:56 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 24 Apr 2020 14:41:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 14:41:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85169d009bd5f0c0ab3d615ff03bc83196402a467630fd52b525956c374af54`  
		Last Modified: Fri, 24 Apr 2020 14:42:25 GMT  
		Size: 16.6 MB (16598643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255366c4ce6923eee6adadbec2d9183c32883ccbb872f78f55012ca66353ef28`  
		Last Modified: Fri, 24 Apr 2020 14:42:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0fb6e436ba41bf7cfedcc84ac2aa94b71cf21e4a8bdea8a172cc1d441dd954`  
		Last Modified: Fri, 24 Apr 2020 14:42:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:37209854c827a1578cd47e7ec80d72025b42abea6c64cd77d0ee03fef79a05dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:7a2b9ba6e6eeb9ea3449effbe4e7144537561758ede01448748bf6ca957ef09d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109929194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354e9f82dd3b6d2f79a7fb61178456e18a6c636a9d384b130e8a375da94bf0c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:43:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:43:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 May 2020 09:44:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 16 May 2020 09:44:18 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 16 May 2020 09:44:31 GMT
ENV KAPACITOR_VERSION=1.5.4
# Sat, 16 May 2020 09:44:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 16 May 2020 09:44:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 May 2020 09:44:35 GMT
EXPOSE 9092
# Sat, 16 May 2020 09:44:35 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 May 2020 09:44:36 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 16 May 2020 09:44:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 May 2020 09:44:36 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b194b0e3c928807cfabf081055a117585ba5bf6697f65b2fede02225a5d73ad2`  
		Last Modified: Fri, 15 May 2020 17:55:27 GMT  
		Size: 10.8 MB (10797475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ec00f35d5b2d1db6b8e925a3005c1a285365775028db0339903ddaeec4763`  
		Last Modified: Fri, 15 May 2020 17:55:29 GMT  
		Size: 4.3 MB (4340139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384f0606b9fbbbd98395f99922e252f11cfa34e5a6630c12b5f0487f7f17011`  
		Last Modified: Sat, 16 May 2020 09:44:50 GMT  
		Size: 13.1 MB (13102550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12c2bdba4f53fc9ba35acf2ec0682e9c71eabd9e0ea0f1e02e575885c572d2f`  
		Last Modified: Sat, 16 May 2020 09:44:48 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7da84fef47ce03360225d6d24cc691e5063e12b3bfdf12faa2a55970d8390b1`  
		Last Modified: Sat, 16 May 2020 09:45:04 GMT  
		Size: 36.3 MB (36310594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f8a9626dbb2ed33f0765a392b9c6ff226301b0ec73018270ce740e4b222c5`  
		Last Modified: Sat, 16 May 2020 09:44:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7cba1fa962e0ffc68caa8d1fa5f066cb67b94e5f2e079147d57aa6574a6569`  
		Last Modified: Sat, 16 May 2020 09:44:58 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:78780b4961a35643ab5e91248b6ae07e749226060cddf90dd5575bdb5a6e2abe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102797996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a35df4341f3394211d645b6c019c6019babd09f927c4a953174f051a34df95f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:07 GMT
ADD file:c0b9ed1244ec0acfc9054c7cb80c768878e3da99740f981ba3a82bdd854305db in / 
# Tue, 09 Jun 2020 01:06:09 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:02:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:02:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:12:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:12:27 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:12:46 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 09 Jun 2020 21:12:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 09 Jun 2020 21:12:54 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:12:54 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:12:55 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:12:56 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:12:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2566ca784846d2d0d4f9105084d94d68d8ea1a82a06a76c5bcd991ce5a10cda1`  
		Last Modified: Tue, 09 Jun 2020 01:13:35 GMT  
		Size: 42.1 MB (42102504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f976b5a12722f5e6e115157695654d36452b713c7fa64a860f8c9e14859402`  
		Last Modified: Tue, 09 Jun 2020 02:15:15 GMT  
		Size: 9.4 MB (9443335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35142ef6ea6c722cd0397799ab151e5da354eabc784b3acef29def7fa34e9bc`  
		Last Modified: Tue, 09 Jun 2020 02:15:13 GMT  
		Size: 3.9 MB (3918433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746389951d399e64371b3fed79516bd9416316ccb7e0a6cbfa8a9e08e546dacb`  
		Last Modified: Tue, 09 Jun 2020 21:13:14 GMT  
		Size: 13.3 MB (13281228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871c5b3b4857aae8365c881c8544b09dd2934c439a97a93284f6a5a47a36bb0`  
		Last Modified: Tue, 09 Jun 2020 21:13:12 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50c1df99f160168b30059be59e5fd9add810a7f9ae10fafd6d461da749470f5`  
		Last Modified: Tue, 09 Jun 2020 21:13:35 GMT  
		Size: 34.0 MB (34049234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55e4c4f931a126157b25fe324f71096fc70a234a6ca62a0ae50e9a2db57b123`  
		Last Modified: Tue, 09 Jun 2020 21:13:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf5ecc983c96851f437721a5a602637abd4da61a094a5f5406956d4492cae0b`  
		Last Modified: Tue, 09 Jun 2020 21:13:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5808fee7acb1c9412f92a18f967dd548a7f607a9146d63cb4a7ecb1469844256
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103827238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af349ac79a76d5d2f7cd329fc4586cbe93092aa9b4dc443c093aad49f929b94a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:53:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:53:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:53:46 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 09 Jun 2020 21:53:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 09 Jun 2020 21:53:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:53:57 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:53:59 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:54:00 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:54:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:54:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0990c417a21ef9e268cc0822cd23968c4b17cded8170cce0c4d8f7e020e6fd`  
		Last Modified: Tue, 09 Jun 2020 02:50:17 GMT  
		Size: 9.7 MB (9699635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6b83fd41426d182f67fdac882a6bfcd3aad22d7226a653ae58d3046bd46b5e`  
		Last Modified: Tue, 09 Jun 2020 02:50:15 GMT  
		Size: 4.1 MB (4094104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba4c6acba469b82e3b6632aaecd1c975cfdad5cd4bd72880d93d97b0eff4282`  
		Last Modified: Tue, 09 Jun 2020 21:54:20 GMT  
		Size: 12.8 MB (12820241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fa9a95920831056c7d3dfc1b43b1c057680d0e4d91c5b72513f527a8ebb2f5`  
		Last Modified: Tue, 09 Jun 2020 21:54:19 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba14a74b222e43ef052c3b5c2c02da86f359b8225900db70c8065462d9baa23c`  
		Last Modified: Tue, 09 Jun 2020 21:54:39 GMT  
		Size: 34.0 MB (34049072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40828b378212b5f4830f152d6dd8d55d30b158c379e615790b94cb36d6967ddf`  
		Last Modified: Tue, 09 Jun 2020 21:54:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0037b9b3f3c323f1ffeffb3a1999425e2d2675a92cf9ccfefb75f888eeb815`  
		Last Modified: Tue, 09 Jun 2020 21:54:30 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.4`

```console
$ docker pull kapacitor@sha256:37209854c827a1578cd47e7ec80d72025b42abea6c64cd77d0ee03fef79a05dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:7a2b9ba6e6eeb9ea3449effbe4e7144537561758ede01448748bf6ca957ef09d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109929194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354e9f82dd3b6d2f79a7fb61178456e18a6c636a9d384b130e8a375da94bf0c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:43:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:43:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 May 2020 09:44:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 16 May 2020 09:44:18 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 16 May 2020 09:44:31 GMT
ENV KAPACITOR_VERSION=1.5.4
# Sat, 16 May 2020 09:44:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 16 May 2020 09:44:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 May 2020 09:44:35 GMT
EXPOSE 9092
# Sat, 16 May 2020 09:44:35 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 May 2020 09:44:36 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 16 May 2020 09:44:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 May 2020 09:44:36 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b194b0e3c928807cfabf081055a117585ba5bf6697f65b2fede02225a5d73ad2`  
		Last Modified: Fri, 15 May 2020 17:55:27 GMT  
		Size: 10.8 MB (10797475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ec00f35d5b2d1db6b8e925a3005c1a285365775028db0339903ddaeec4763`  
		Last Modified: Fri, 15 May 2020 17:55:29 GMT  
		Size: 4.3 MB (4340139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384f0606b9fbbbd98395f99922e252f11cfa34e5a6630c12b5f0487f7f17011`  
		Last Modified: Sat, 16 May 2020 09:44:50 GMT  
		Size: 13.1 MB (13102550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12c2bdba4f53fc9ba35acf2ec0682e9c71eabd9e0ea0f1e02e575885c572d2f`  
		Last Modified: Sat, 16 May 2020 09:44:48 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7da84fef47ce03360225d6d24cc691e5063e12b3bfdf12faa2a55970d8390b1`  
		Last Modified: Sat, 16 May 2020 09:45:04 GMT  
		Size: 36.3 MB (36310594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f8a9626dbb2ed33f0765a392b9c6ff226301b0ec73018270ce740e4b222c5`  
		Last Modified: Sat, 16 May 2020 09:44:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7cba1fa962e0ffc68caa8d1fa5f066cb67b94e5f2e079147d57aa6574a6569`  
		Last Modified: Sat, 16 May 2020 09:44:58 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:78780b4961a35643ab5e91248b6ae07e749226060cddf90dd5575bdb5a6e2abe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102797996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a35df4341f3394211d645b6c019c6019babd09f927c4a953174f051a34df95f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:07 GMT
ADD file:c0b9ed1244ec0acfc9054c7cb80c768878e3da99740f981ba3a82bdd854305db in / 
# Tue, 09 Jun 2020 01:06:09 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:02:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:02:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:12:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:12:27 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:12:46 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 09 Jun 2020 21:12:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 09 Jun 2020 21:12:54 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:12:54 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:12:55 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:12:56 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:12:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2566ca784846d2d0d4f9105084d94d68d8ea1a82a06a76c5bcd991ce5a10cda1`  
		Last Modified: Tue, 09 Jun 2020 01:13:35 GMT  
		Size: 42.1 MB (42102504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f976b5a12722f5e6e115157695654d36452b713c7fa64a860f8c9e14859402`  
		Last Modified: Tue, 09 Jun 2020 02:15:15 GMT  
		Size: 9.4 MB (9443335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35142ef6ea6c722cd0397799ab151e5da354eabc784b3acef29def7fa34e9bc`  
		Last Modified: Tue, 09 Jun 2020 02:15:13 GMT  
		Size: 3.9 MB (3918433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746389951d399e64371b3fed79516bd9416316ccb7e0a6cbfa8a9e08e546dacb`  
		Last Modified: Tue, 09 Jun 2020 21:13:14 GMT  
		Size: 13.3 MB (13281228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871c5b3b4857aae8365c881c8544b09dd2934c439a97a93284f6a5a47a36bb0`  
		Last Modified: Tue, 09 Jun 2020 21:13:12 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50c1df99f160168b30059be59e5fd9add810a7f9ae10fafd6d461da749470f5`  
		Last Modified: Tue, 09 Jun 2020 21:13:35 GMT  
		Size: 34.0 MB (34049234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55e4c4f931a126157b25fe324f71096fc70a234a6ca62a0ae50e9a2db57b123`  
		Last Modified: Tue, 09 Jun 2020 21:13:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf5ecc983c96851f437721a5a602637abd4da61a094a5f5406956d4492cae0b`  
		Last Modified: Tue, 09 Jun 2020 21:13:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5808fee7acb1c9412f92a18f967dd548a7f607a9146d63cb4a7ecb1469844256
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103827238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af349ac79a76d5d2f7cd329fc4586cbe93092aa9b4dc443c093aad49f929b94a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:53:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:53:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:53:46 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 09 Jun 2020 21:53:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 09 Jun 2020 21:53:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:53:57 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:53:59 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:54:00 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:54:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:54:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0990c417a21ef9e268cc0822cd23968c4b17cded8170cce0c4d8f7e020e6fd`  
		Last Modified: Tue, 09 Jun 2020 02:50:17 GMT  
		Size: 9.7 MB (9699635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6b83fd41426d182f67fdac882a6bfcd3aad22d7226a653ae58d3046bd46b5e`  
		Last Modified: Tue, 09 Jun 2020 02:50:15 GMT  
		Size: 4.1 MB (4094104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba4c6acba469b82e3b6632aaecd1c975cfdad5cd4bd72880d93d97b0eff4282`  
		Last Modified: Tue, 09 Jun 2020 21:54:20 GMT  
		Size: 12.8 MB (12820241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fa9a95920831056c7d3dfc1b43b1c057680d0e4d91c5b72513f527a8ebb2f5`  
		Last Modified: Tue, 09 Jun 2020 21:54:19 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba14a74b222e43ef052c3b5c2c02da86f359b8225900db70c8065462d9baa23c`  
		Last Modified: Tue, 09 Jun 2020 21:54:39 GMT  
		Size: 34.0 MB (34049072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40828b378212b5f4830f152d6dd8d55d30b158c379e615790b94cb36d6967ddf`  
		Last Modified: Tue, 09 Jun 2020 21:54:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0037b9b3f3c323f1ffeffb3a1999425e2d2675a92cf9ccfefb75f888eeb815`  
		Last Modified: Tue, 09 Jun 2020 21:54:30 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.4-alpine`

```console
$ docker pull kapacitor@sha256:5a15b4f278b22929cf11ebc0c58e717f6600349de81e6ca80d37316a5f265cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:aa605c5e74ff149da7d84f26a0d79ae92ae12038ce4086343482769df205e973
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23100428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cacac6e6e047ea1cb9bbd65a0aac14f532c60c336f82dad553a938c07548fbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 14:42:04 GMT
ENV KAPACITOR_VERSION=1.5.4
# Fri, 24 Apr 2020 14:42:08 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Apr 2020 14:42:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 24 Apr 2020 14:42:09 GMT
EXPOSE 9092
# Fri, 24 Apr 2020 14:42:09 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 24 Apr 2020 14:42:09 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 24 Apr 2020 14:42:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 14:42:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161ba29b8c4be210a2aa0d6aff44ea1a8e7654e8a76c5c49cd153af81c6fccc8`  
		Last Modified: Fri, 24 Apr 2020 14:42:32 GMT  
		Size: 20.0 MB (20025317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4451a41250e65170a52cf51e2d450bd5fd2b0ef564f5775e45079116b08e31`  
		Last Modified: Fri, 24 Apr 2020 14:42:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee9620905de433be23893da5c25b38efa5c05ea4d28122e98137b6c7d1e37a`  
		Last Modified: Fri, 24 Apr 2020 14:42:29 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:5a15b4f278b22929cf11ebc0c58e717f6600349de81e6ca80d37316a5f265cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:aa605c5e74ff149da7d84f26a0d79ae92ae12038ce4086343482769df205e973
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23100428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cacac6e6e047ea1cb9bbd65a0aac14f532c60c336f82dad553a938c07548fbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 14:42:04 GMT
ENV KAPACITOR_VERSION=1.5.4
# Fri, 24 Apr 2020 14:42:08 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Apr 2020 14:42:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 24 Apr 2020 14:42:09 GMT
EXPOSE 9092
# Fri, 24 Apr 2020 14:42:09 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 24 Apr 2020 14:42:09 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 24 Apr 2020 14:42:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 14:42:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161ba29b8c4be210a2aa0d6aff44ea1a8e7654e8a76c5c49cd153af81c6fccc8`  
		Last Modified: Fri, 24 Apr 2020 14:42:32 GMT  
		Size: 20.0 MB (20025317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4451a41250e65170a52cf51e2d450bd5fd2b0ef564f5775e45079116b08e31`  
		Last Modified: Fri, 24 Apr 2020 14:42:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee9620905de433be23893da5c25b38efa5c05ea4d28122e98137b6c7d1e37a`  
		Last Modified: Fri, 24 Apr 2020 14:42:29 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:5a15b4f278b22929cf11ebc0c58e717f6600349de81e6ca80d37316a5f265cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:aa605c5e74ff149da7d84f26a0d79ae92ae12038ce4086343482769df205e973
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23100428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cacac6e6e047ea1cb9bbd65a0aac14f532c60c336f82dad553a938c07548fbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 14:42:04 GMT
ENV KAPACITOR_VERSION=1.5.4
# Fri, 24 Apr 2020 14:42:08 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Apr 2020 14:42:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 24 Apr 2020 14:42:09 GMT
EXPOSE 9092
# Fri, 24 Apr 2020 14:42:09 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 24 Apr 2020 14:42:09 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 24 Apr 2020 14:42:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 14:42:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161ba29b8c4be210a2aa0d6aff44ea1a8e7654e8a76c5c49cd153af81c6fccc8`  
		Last Modified: Fri, 24 Apr 2020 14:42:32 GMT  
		Size: 20.0 MB (20025317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4451a41250e65170a52cf51e2d450bd5fd2b0ef564f5775e45079116b08e31`  
		Last Modified: Fri, 24 Apr 2020 14:42:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee9620905de433be23893da5c25b38efa5c05ea4d28122e98137b6c7d1e37a`  
		Last Modified: Fri, 24 Apr 2020 14:42:29 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:37209854c827a1578cd47e7ec80d72025b42abea6c64cd77d0ee03fef79a05dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:7a2b9ba6e6eeb9ea3449effbe4e7144537561758ede01448748bf6ca957ef09d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109929194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354e9f82dd3b6d2f79a7fb61178456e18a6c636a9d384b130e8a375da94bf0c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:43:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:43:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 May 2020 09:44:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 16 May 2020 09:44:18 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 16 May 2020 09:44:31 GMT
ENV KAPACITOR_VERSION=1.5.4
# Sat, 16 May 2020 09:44:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 16 May 2020 09:44:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 May 2020 09:44:35 GMT
EXPOSE 9092
# Sat, 16 May 2020 09:44:35 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 May 2020 09:44:36 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 16 May 2020 09:44:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 May 2020 09:44:36 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b194b0e3c928807cfabf081055a117585ba5bf6697f65b2fede02225a5d73ad2`  
		Last Modified: Fri, 15 May 2020 17:55:27 GMT  
		Size: 10.8 MB (10797475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ec00f35d5b2d1db6b8e925a3005c1a285365775028db0339903ddaeec4763`  
		Last Modified: Fri, 15 May 2020 17:55:29 GMT  
		Size: 4.3 MB (4340139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384f0606b9fbbbd98395f99922e252f11cfa34e5a6630c12b5f0487f7f17011`  
		Last Modified: Sat, 16 May 2020 09:44:50 GMT  
		Size: 13.1 MB (13102550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12c2bdba4f53fc9ba35acf2ec0682e9c71eabd9e0ea0f1e02e575885c572d2f`  
		Last Modified: Sat, 16 May 2020 09:44:48 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7da84fef47ce03360225d6d24cc691e5063e12b3bfdf12faa2a55970d8390b1`  
		Last Modified: Sat, 16 May 2020 09:45:04 GMT  
		Size: 36.3 MB (36310594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f8a9626dbb2ed33f0765a392b9c6ff226301b0ec73018270ce740e4b222c5`  
		Last Modified: Sat, 16 May 2020 09:44:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7cba1fa962e0ffc68caa8d1fa5f066cb67b94e5f2e079147d57aa6574a6569`  
		Last Modified: Sat, 16 May 2020 09:44:58 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:78780b4961a35643ab5e91248b6ae07e749226060cddf90dd5575bdb5a6e2abe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102797996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a35df4341f3394211d645b6c019c6019babd09f927c4a953174f051a34df95f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:07 GMT
ADD file:c0b9ed1244ec0acfc9054c7cb80c768878e3da99740f981ba3a82bdd854305db in / 
# Tue, 09 Jun 2020 01:06:09 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:02:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:02:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:12:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:12:27 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:12:46 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 09 Jun 2020 21:12:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 09 Jun 2020 21:12:54 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:12:54 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:12:55 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:12:56 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:12:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2566ca784846d2d0d4f9105084d94d68d8ea1a82a06a76c5bcd991ce5a10cda1`  
		Last Modified: Tue, 09 Jun 2020 01:13:35 GMT  
		Size: 42.1 MB (42102504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f976b5a12722f5e6e115157695654d36452b713c7fa64a860f8c9e14859402`  
		Last Modified: Tue, 09 Jun 2020 02:15:15 GMT  
		Size: 9.4 MB (9443335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35142ef6ea6c722cd0397799ab151e5da354eabc784b3acef29def7fa34e9bc`  
		Last Modified: Tue, 09 Jun 2020 02:15:13 GMT  
		Size: 3.9 MB (3918433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746389951d399e64371b3fed79516bd9416316ccb7e0a6cbfa8a9e08e546dacb`  
		Last Modified: Tue, 09 Jun 2020 21:13:14 GMT  
		Size: 13.3 MB (13281228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871c5b3b4857aae8365c881c8544b09dd2934c439a97a93284f6a5a47a36bb0`  
		Last Modified: Tue, 09 Jun 2020 21:13:12 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50c1df99f160168b30059be59e5fd9add810a7f9ae10fafd6d461da749470f5`  
		Last Modified: Tue, 09 Jun 2020 21:13:35 GMT  
		Size: 34.0 MB (34049234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55e4c4f931a126157b25fe324f71096fc70a234a6ca62a0ae50e9a2db57b123`  
		Last Modified: Tue, 09 Jun 2020 21:13:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf5ecc983c96851f437721a5a602637abd4da61a094a5f5406956d4492cae0b`  
		Last Modified: Tue, 09 Jun 2020 21:13:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5808fee7acb1c9412f92a18f967dd548a7f607a9146d63cb4a7ecb1469844256
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103827238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af349ac79a76d5d2f7cd329fc4586cbe93092aa9b4dc443c093aad49f929b94a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 21:53:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 09 Jun 2020 21:53:22 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Jun 2020 21:53:46 GMT
ENV KAPACITOR_VERSION=1.5.4
# Tue, 09 Jun 2020 21:53:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 09 Jun 2020 21:53:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 09 Jun 2020 21:53:57 GMT
EXPOSE 9092
# Tue, 09 Jun 2020 21:53:59 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 09 Jun 2020 21:54:00 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 09 Jun 2020 21:54:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 21:54:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0990c417a21ef9e268cc0822cd23968c4b17cded8170cce0c4d8f7e020e6fd`  
		Last Modified: Tue, 09 Jun 2020 02:50:17 GMT  
		Size: 9.7 MB (9699635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6b83fd41426d182f67fdac882a6bfcd3aad22d7226a653ae58d3046bd46b5e`  
		Last Modified: Tue, 09 Jun 2020 02:50:15 GMT  
		Size: 4.1 MB (4094104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba4c6acba469b82e3b6632aaecd1c975cfdad5cd4bd72880d93d97b0eff4282`  
		Last Modified: Tue, 09 Jun 2020 21:54:20 GMT  
		Size: 12.8 MB (12820241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fa9a95920831056c7d3dfc1b43b1c057680d0e4d91c5b72513f527a8ebb2f5`  
		Last Modified: Tue, 09 Jun 2020 21:54:19 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba14a74b222e43ef052c3b5c2c02da86f359b8225900db70c8065462d9baa23c`  
		Last Modified: Tue, 09 Jun 2020 21:54:39 GMT  
		Size: 34.0 MB (34049072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40828b378212b5f4830f152d6dd8d55d30b158c379e615790b94cb36d6967ddf`  
		Last Modified: Tue, 09 Jun 2020 21:54:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0037b9b3f3c323f1ffeffb3a1999425e2d2675a92cf9ccfefb75f888eeb815`  
		Last Modified: Tue, 09 Jun 2020 21:54:30 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
