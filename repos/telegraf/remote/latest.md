## `telegraf:latest`

```console
$ docker pull telegraf@sha256:859a8f04192cc55b9f749042168e0019d6b5bb4aa5f4e07b19e1f3faef78b706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:f1b1cd261ac8f203b6c060851890c48b8c6f6972e52883a3e278da3d63dd21e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130236042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b6334dd66b1a1750cce92d083eb30855ec760b5b38209386edbaf489f00053`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 May 2022 01:20:05 GMT
ADD file:68a5d7d0db592625159865110c1b7dcb15cf70ecf71b5fd541ef89584cd734ba in / 
# Wed, 11 May 2022 01:20:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:49:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:49:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 20:43:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 20:43:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 20:43:42 GMT
ENV TELEGRAF_VERSION=1.22.3
# Wed, 11 May 2022 20:43:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 11 May 2022 20:43:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 11 May 2022 20:43:46 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 11 May 2022 20:43:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 20:43:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:67e8aa6c8bbc76b1f2bccb3864b0887671833b8667dc1f6c965fcb0eac7e6402`  
		Last Modified: Wed, 11 May 2022 01:24:45 GMT  
		Size: 54.9 MB (54945622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627e6c1e105548ea4a08354eea581f137cf368d91aeb0ad47dcb706fca54fd8b`  
		Last Modified: Wed, 11 May 2022 01:57:17 GMT  
		Size: 5.2 MB (5155721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0670968926f6461e3135c82ba2c0ad3ebdedc0d0f41b18bda4a1e41104b8be8a`  
		Last Modified: Wed, 11 May 2022 01:57:18 GMT  
		Size: 10.9 MB (10875052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d362a0af2235ab1dbf54bed2a8fe86542d2bf72d986366bf43b9fa418d7770b7`  
		Last Modified: Wed, 11 May 2022 20:44:10 GMT  
		Size: 18.8 MB (18760176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75e1b3581e02b679d4b9318bd0ee7b6906ca0abd0cf9a6d6a487bd81b208984`  
		Last Modified: Wed, 11 May 2022 20:44:06 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be3330127dcf040673aa2983385f7771a38b63a0185873e1af4cd478592de1a`  
		Last Modified: Wed, 11 May 2022 20:44:55 GMT  
		Size: 40.5 MB (40496227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a4414d85bf59c1798885ef379bad0173b5f98eb7dc4fc13bdcbcde115d51f5`  
		Last Modified: Wed, 11 May 2022 20:44:43 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:68c81e64109ab94b59e14845b0e4f7c7c5b4f127c853edf6c947f4c1486d12d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120677776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c91544bf5273e9d69bbd188d7d2935653e1b41248dd8cddc2a74402b258ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 May 2022 01:48:30 GMT
ADD file:d6545064ea0f75166d59e4d4a2df1e41a3477ae468e558e31f29857336978c0e in / 
# Wed, 11 May 2022 01:48:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:21:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:21:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 12 May 2022 15:38:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 15:38:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 May 2022 15:38:59 GMT
ENV TELEGRAF_VERSION=1.22.3
# Thu, 12 May 2022 15:39:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 May 2022 15:39:12 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 May 2022 15:39:12 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 May 2022 15:39:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 May 2022 15:39:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ba38f9a6c66968e207a7ada348a2110e3be0ff117e621d9e10ddd7c4becc0d2a`  
		Last Modified: Wed, 11 May 2022 02:03:49 GMT  
		Size: 50.1 MB (50134069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71423015d7b4f718e54ff1561cc06bb4c8357baedc23b49d25fe99cd4b0ae41`  
		Last Modified: Wed, 11 May 2022 03:46:39 GMT  
		Size: 4.9 MB (4924901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f92194faa0a66e5bd160b229941428f0b0387c6e313e4f1f903c678fbb17e`  
		Last Modified: Wed, 11 May 2022 03:46:41 GMT  
		Size: 10.2 MB (10217886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9e807a9fc03351b3973a60a2adaa8720bc827e059c98ea3640bd76215f2cf9`  
		Last Modified: Thu, 12 May 2022 15:40:09 GMT  
		Size: 17.5 MB (17462466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1518832bed87bf762c281236f0a5db851229537fa149fd3980df84cebf1e6f94`  
		Last Modified: Thu, 12 May 2022 15:39:56 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bedef9fd7ef850a5002d7ef2777da7ae3a01a01b6bcbf36a1559179febd9f3`  
		Last Modified: Thu, 12 May 2022 15:41:35 GMT  
		Size: 37.9 MB (37935221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fda29a35a251676f744ffffe4785f738d18b11d5178ff8f931bad7e3dcb33a`  
		Last Modified: Thu, 12 May 2022 15:41:08 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:906b1627f4e75e00ef530375c5ec11d581a523acd1d482c77f2cb334fbb6001b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124422229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c498859ee7bad23bd6e231309cfa1f53ff247a11c3a2c35716c15136c3b339`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 May 2022 00:46:44 GMT
ADD file:239aa42118877a929b2fbfc0d5793fee7815289280affa5286de2459385c0679 in / 
# Wed, 11 May 2022 00:46:44 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:25:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:25:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 19:38:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 19:38:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 19:38:34 GMT
ENV TELEGRAF_VERSION=1.22.3
# Wed, 11 May 2022 19:38:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 11 May 2022 19:38:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 11 May 2022 19:38:42 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 11 May 2022 19:38:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 19:38:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3a36574378e6cece2dd3a839e1c0220eaccc4063b61d7481d1a19d3990c1f2c2`  
		Last Modified: Wed, 11 May 2022 00:53:15 GMT  
		Size: 53.6 MB (53634337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d3345afba43846f3e638752cce2f0d1d47b21cc667ba08b00db10767a4702`  
		Last Modified: Wed, 11 May 2022 01:35:45 GMT  
		Size: 4.9 MB (4938615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e267d6aa58f93a513352a3b46c7addbf9335d7d43bfa4f1df4026d21785181c`  
		Last Modified: Wed, 11 May 2022 01:35:46 GMT  
		Size: 10.7 MB (10656992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9acc4c089b6be76ee1116d879fed702822f77839c7ed661db98071eadefa9d`  
		Last Modified: Wed, 11 May 2022 19:39:08 GMT  
		Size: 18.4 MB (18382761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b25798f80aae6c051b16fbbf074531ba36c89a5b5aa95ad52abb2cd2bd8a0c`  
		Last Modified: Wed, 11 May 2022 19:39:05 GMT  
		Size: 2.9 KB (2868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e829fc81cc3d586cf2e95be793b77158689b38d4a1b7e1cac69395ce19d27`  
		Last Modified: Wed, 11 May 2022 19:39:49 GMT  
		Size: 36.8 MB (36806312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3485bf2d65be5fb85eeca368baab92256c78da396d72c01f842924332a36de7d`  
		Last Modified: Wed, 11 May 2022 19:39:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
