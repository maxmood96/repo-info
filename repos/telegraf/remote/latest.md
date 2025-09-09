## `telegraf:latest`

```console
$ docker pull telegraf@sha256:bfe0a116f05de4257c071e2b912b8835f4f894e5009324a8e881dbc1c257af10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:fd45e1d1713e1f4a189f58adb0e3bb990388054a8c05b8b7bd40265a3ba8b0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171242086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5391e161b50cabc3a294af8f066a133637ba3c5952a29044e00ab536f737ddcc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c2ee446e0b5bbdfe651f8e8a947c6da99475770aacba32d83156a92dc224bd`  
		Last Modified: Tue, 09 Sep 2025 00:10:46 GMT  
		Size: 18.9 MB (18942743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485ea33a36258d7f06e4548b5e7c0dc7cb4517f659c372057cafb5977ce27c6`  
		Last Modified: Mon, 08 Sep 2025 23:21:28 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d02dfb1e8e097b292ae6245bd5355535dc759bf8e6915d003bf63ae4bc3514`  
		Last Modified: Tue, 09 Sep 2025 00:10:50 GMT  
		Size: 79.8 MB (79790329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef7eff07ccf38016fce817cbf6236870952ff975e62a5ea2a252b52aa6246b5`  
		Last Modified: Mon, 08 Sep 2025 23:21:32 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:480803422cc9df0d8ae0b64688b0cd583a2ca70c5149cd11ffb7391cfdf4dbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f989ee600ffa69e8527cfc3b08477f5df6877e6fa6ada1ba85cfc676a34fc97`

```dockerfile
```

-	Layers:
	-	`sha256:38f8df255fc19c30a1b2c093d0871e3e8d49ba059cbb35f851f699685ca9de65`  
		Last Modified: Tue, 09 Sep 2025 00:10:35 GMT  
		Size: 6.6 MB (6647004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f24b7f6bdd42b8290ccd785bda01ec46b8535fcefa59c9347cdf7e030a1fa5`  
		Last Modified: Tue, 09 Sep 2025 00:10:36 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:6f1e156f9ba35b0c4fbfc560e1d1a970018ad55136b70fca3b93a1f22cb00901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157245348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e523b7d1d3f47e63da901c640e5a2a21e815c8ca0a3ba25e019066150c1ef664`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf37909f7ac4e3f15c2c7ecacc16fa58ef82d28624bff9276a057663fd0976d`  
		Last Modified: Tue, 09 Sep 2025 04:48:49 GMT  
		Size: 17.7 MB (17722690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357da611076f9bea097256a99992d403698e61db6ab4457d659bac12e58128f0`  
		Last Modified: Tue, 09 Sep 2025 04:17:08 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb0d2a9d377a19d06964706a4d17bfdbe89817368efd35ab26f960e67f074b5`  
		Last Modified: Tue, 09 Sep 2025 06:16:26 GMT  
		Size: 73.4 MB (73393187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925b60c2429fcfe053fa357672b92a9ef0312eadb39ee79a57fc1501dcb0c40f`  
		Last Modified: Tue, 09 Sep 2025 04:17:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:a89b5bb15ca9c81b168f04f65af123d104dc9de7f03cc75cbe8c4ff7f2b899aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebf7d439bea332dc983877d0abdf722422cc2df7f14341b438b18e2b10a0d4e`

```dockerfile
```

-	Layers:
	-	`sha256:3a12b16a293fe0fb5be1024302575a94f36f668b77c1418e7578245d7182a783`  
		Last Modified: Tue, 09 Sep 2025 06:10:40 GMT  
		Size: 6.6 MB (6641609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0287306c6a36fa7761e95df155193fee70867cdd779051d5c3be3d47c8341727`  
		Last Modified: Tue, 09 Sep 2025 06:10:41 GMT  
		Size: 14.9 KB (14869 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0523d06ce0843d29e2d8f224e3d38267b5ccda09e195d42c9890701908059e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162052135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3827a84def9d7d257577bbada5dcee1dd5664e11852964e902245fe27f1296`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6164fcfed84e1c4e85e432856b2a87eb600a74e1a3593495b5cbf37306be6b68`  
		Last Modified: Tue, 09 Sep 2025 02:30:08 GMT  
		Size: 18.9 MB (18884019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5c0bc84f09aa9905cb1e2686725a41008b57dcb1f04d9981c6f9cdbc303b0c`  
		Last Modified: Tue, 09 Sep 2025 02:23:20 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c9ec34b7c0601f78e378ca8a39adc94ebe24a8e60614e5dd4f97a6bda21dea`  
		Last Modified: Tue, 09 Sep 2025 02:30:11 GMT  
		Size: 71.2 MB (71211897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fea26294569d3d04727fc0f8cd7c42b978e0825eb40ef965d5857a8ea2a95c`  
		Last Modified: Tue, 09 Sep 2025 02:23:19 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7a45a99cf5874d166b9ffc8252efde13f233b125256b1babc5021cb71ce17e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f291bc4a2338b84d5cf160df7fd0506ceee989b28d30b8a98915440f84082f0`

```dockerfile
```

-	Layers:
	-	`sha256:517b563a6a20b522f8a3d37cebf314584cbdaca4610189cea638097a7a77c536`  
		Last Modified: Tue, 09 Sep 2025 03:10:38 GMT  
		Size: 6.6 MB (6647692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ccb47971f161945c59e8d2260543720693ce1e3e401d200dfdc78ebde51e7b`  
		Last Modified: Tue, 09 Sep 2025 03:10:39 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
