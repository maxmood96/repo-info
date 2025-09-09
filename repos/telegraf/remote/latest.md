## `telegraf:latest`

```console
$ docker pull telegraf@sha256:2e18ff525e2901055234570c2c273bac86dd98ec0b16eb644593f3823c93e9c4
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
$ docker pull telegraf@sha256:91b8d30fa4be79a13d9f51dd4816ba0fc0a695a7d36b72af073c9749e63bf5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157156497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993e5a766b756ccfd7713920c7a9a1b14ab87dd3e0f341bb2ddfd1b604657562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fdff4dcb6359e721989060c3743deca10d1e73cef0d9b907513c9b4f320f4`  
		Last Modified: Wed, 13 Aug 2025 11:56:52 GMT  
		Size: 17.7 MB (17725068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797481eb709a7b6a93b1cc1814d1f5184123c7245ebd3cdd2c05ae8ebfff5d30`  
		Last Modified: Wed, 13 Aug 2025 11:14:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637ea78bbab9b8889bcfddd80e42dd1798df1e3424c850924021be81254882cd`  
		Last Modified: Tue, 19 Aug 2025 16:42:43 GMT  
		Size: 73.3 MB (73290612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d2045f5208fe2cbc05be97c6a6f0cf96d5bd336067d64a1167223bf6c7d38`  
		Last Modified: Tue, 19 Aug 2025 16:42:20 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb8b802448d044c19b6bade15fe09c2513c1d83bca7e3ad2207f4ebd833bc6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d204ca9c7f06d1ca0dc1771646db5b6fe4d78803adaed77dfcc4a5a9690a82`

```dockerfile
```

-	Layers:
	-	`sha256:974c18a6fda81be68b50b13dea7c3313a417a56c1921c4d5e83409087c5a9a81`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 6.6 MB (6633080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196854c3e97335eeb6c8e0e3bad45237633e6e0cbeb761abb7a6f8208021332c`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 14.9 KB (14866 bytes)  
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
