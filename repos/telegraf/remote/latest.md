## `telegraf:latest`

```console
$ docker pull telegraf@sha256:69f8bf839f269b140f520645df55a12d0011e4c31686e4379e9e991b6017deeb
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
$ docker pull telegraf@sha256:f6c305c9aa52a779821a405ffecb8f937a66a42aee057e238d9fc069ce542264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171670812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5faeffe443a351fab33a32ba7e4cb226adb2bf8e282facd6e6de01563c749514`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81574d2b1469f48c4abb9c4b5b903a9a61648837e305523823879d8b6f42e965`  
		Last Modified: Tue, 21 Oct 2025 05:00:18 GMT  
		Size: 18.9 MB (18942783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9253b805ed21ce9fbdd67a334bdaa5a03288a512a2e1256461e28f4649723fc6`  
		Last Modified: Tue, 21 Oct 2025 05:00:17 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca145bdde161b45d021a458f1f862c506046273b93d0f0a67a4aa9fd59c7ab7`  
		Last Modified: Tue, 21 Oct 2025 05:00:29 GMT  
		Size: 80.2 MB (80214495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd83b81e8663dcdafe6029619930455860e8fea7376e1a1e087517401eb007c3`  
		Last Modified: Tue, 21 Oct 2025 05:00:17 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:5ac9998111fb4b214f8a51579a78be59911843e5b7f2d09541ee416bbdcede70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e672b4b327600235582018f05140f270f6a888303273b78384f21a755c55b0`

```dockerfile
```

-	Layers:
	-	`sha256:b3667c89351080a25f1b2154351e5a2338f4ec03b02f5acf03cf5f560f16e609`  
		Last Modified: Tue, 21 Oct 2025 09:10:56 GMT  
		Size: 6.7 MB (6651978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a36ffed979f620b23cbf342a0d60bd596f8aae19a085f23c8d9e5596bbd751`  
		Last Modified: Tue, 21 Oct 2025 09:10:57 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1dee607996b7ed9360bb62cb57b962bae24e9688dc8324aeb50233bdeac73a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157638733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aec8c04b49e6236e48f520ce74bc799e1d4dbed03f99108c17bc13a7e41f776`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774eb8b0193c2a3f9cbe631908908602c0e5522f1779cadd86467e43fc50d948`  
		Last Modified: Tue, 21 Oct 2025 04:22:52 GMT  
		Size: 17.7 MB (17722588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe485ded5c46cc0e8b583b8c73b9253fd36ea66b1fb84718c2304f0611585dc`  
		Last Modified: Tue, 21 Oct 2025 04:22:47 GMT  
		Size: 3.5 KB (3451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053849f85a0f2fac026f3cd9b83f9a40a563b643067b7b18c266b56ca1621b1`  
		Last Modified: Tue, 21 Oct 2025 04:23:02 GMT  
		Size: 73.8 MB (73781657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3dc3f10b5b4cb205671627d71a78f045cf0f7dda313695a8d4710de0980497`  
		Last Modified: Tue, 21 Oct 2025 04:22:48 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:90d9bcad38585f6c5b7e56671741f9379b5bd3f998d45b2ccc1e37190ee2dd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0e56f5926ebd1acabba3e3e01b4e23ebff918ba8b78bd6128e4e54f9681786`

```dockerfile
```

-	Layers:
	-	`sha256:62ffd1e7aec54febdb797812ed153146767561a9ecda80c0227e922fd65fd573`  
		Last Modified: Tue, 21 Oct 2025 09:11:03 GMT  
		Size: 6.6 MB (6646583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a774250545d0354c682d64d7a461d0e4b8a5a601b8449cd4db1c894c901eac46`  
		Last Modified: Tue, 21 Oct 2025 09:11:03 GMT  
		Size: 14.9 KB (14870 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8d39eedbfec74664649141d18e24cc05ffbac743ad1226827603cf4d01fb49fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162403506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cfd0b3f3491d02bc1941f53a3d3927920a4df515b05c4c7235d761b0434cbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ee270eedc40f9608dc63c465be5633d5fef010c988fa97f2412a1e2e119ded`  
		Last Modified: Tue, 21 Oct 2025 02:47:47 GMT  
		Size: 18.9 MB (18883596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33f7f49ca28eb15df6dca101b2eb4e77982888d995ee7018ecd80f649ffa064`  
		Last Modified: Tue, 21 Oct 2025 02:47:46 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941fafeba3aa419837265fc89d6b9721f6ee37dc3de0e9edded3d2b0af88a20d`  
		Last Modified: Tue, 21 Oct 2025 02:48:24 GMT  
		Size: 71.6 MB (71558861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032b6937b97b8fe7dc2bd1b857342fa404c2d4846f22043b3a14eb5b9669c6c6`  
		Last Modified: Tue, 21 Oct 2025 02:48:17 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:c60ce656430741e81beee2bd0154d89117f4e11eb54e29bacdefd98cd2795fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540f35dabdda28c4d456109a3fbb90e8d49f21d5ded783988358c3af7d47ceb9`

```dockerfile
```

-	Layers:
	-	`sha256:c84d64d35a028be188bc8f4ca6aeffbe66c5bca0317a43484053747909ad37dc`  
		Last Modified: Tue, 21 Oct 2025 09:11:09 GMT  
		Size: 6.7 MB (6652666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3875e0f8530da7358bce00afd4244f3a2a001170b0b9fd4ab46ee51431ceac7`  
		Last Modified: Tue, 21 Oct 2025 09:11:10 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
