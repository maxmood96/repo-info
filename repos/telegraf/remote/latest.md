## `telegraf:latest`

```console
$ docker pull telegraf@sha256:2a852f40e95492a3f6ed668999181871c0c05b22c98d2eb56381e9f9ff51596b
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
$ docker pull telegraf@sha256:1079027904b28152199479f1440addefa102a5d2c5a2af2ab3c084e40fae1090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157762926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600b167d82f2e221e018a79e1a35fd37c4cf44f3e6dab990065f5934c97beac9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 21 Oct 2025 12:55:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 Oct 2025 12:55:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
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
	-	`sha256:e98aead9b9ba4196676a2e45d3d6118add7c6b1cd6e8dbcdb2bb4a4d9db3a98f`  
		Last Modified: Tue, 21 Oct 2025 19:44:40 GMT  
		Size: 17.7 MB (17722613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f6eeea3e8874a0cca90be095e157548a995cd486beec1a23ab4a60bbf4ca`  
		Last Modified: Tue, 21 Oct 2025 19:44:26 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32be96b7299c3bea8945b122b94a00a380e0a39ea8ab69cdbc806314379a9719`  
		Last Modified: Tue, 21 Oct 2025 19:44:50 GMT  
		Size: 73.9 MB (73905823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5eb942baf092d8962e22e4a2c167ab180928a04e54e9ffde4322b10d76e199`  
		Last Modified: Tue, 21 Oct 2025 19:44:28 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:eb232558f3055507c3383bb86435f0807b02442c17971c741b10256baf8274cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ff5dd43197b41b503f5e1b7d18ed122bfd2df1565700c2989ca0522ef3317`

```dockerfile
```

-	Layers:
	-	`sha256:7e0ba58aa9a2b04cbaaf382ed7b6c6b945159563bda64c98b4511cb2f2015a54`  
		Last Modified: Tue, 21 Oct 2025 21:10:30 GMT  
		Size: 6.6 MB (6647310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d82e1a06474ebb4db227e304db97914f4410e841928c542b47bcfdff7e9eddfc`  
		Last Modified: Tue, 21 Oct 2025 21:10:30 GMT  
		Size: 14.9 KB (14870 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:65b19e84e9a03767b50bdd634f009e15255b78561f832343350ca6003fac4530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162541564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bde5d33423573a5472c34ef5d0898b82eab152ecaa26f19551d0c3348ca69b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 21 Oct 2025 12:55:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 Oct 2025 12:55:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
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
	-	`sha256:db5d6198d904acd4f7fd09bba9b2c7e5b2a044165e13cdcbf265273115b9d177`  
		Last Modified: Tue, 21 Oct 2025 19:54:26 GMT  
		Size: 18.9 MB (18884363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be438212a6d10204118d0d7025a217e3ee4e18d95e2ec0daecac1f74a4149ecb`  
		Last Modified: Tue, 21 Oct 2025 19:54:24 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6e799e233cc9ff46e6da55a9478a562f2806ad3372aa46990cb02cfe06f0e5`  
		Last Modified: Tue, 21 Oct 2025 19:54:35 GMT  
		Size: 71.7 MB (71696148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a3de341b02aed0b6140706c597bcdbe9fe4d5235cf48ccdb6fca99343d4740`  
		Last Modified: Tue, 21 Oct 2025 19:54:24 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:3141f311236056f8920a7f46b702d69229285758924ba485a67005de5af7e8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cc8339d5cc703276af1ade66f7b5c823b5040bba7cfd495ea80c56bff179e0`

```dockerfile
```

-	Layers:
	-	`sha256:d075eea2efa9ba1f431c134db45332c89eb74a3b3c2867b1eb388b85efc733c8`  
		Last Modified: Tue, 21 Oct 2025 21:10:36 GMT  
		Size: 6.7 MB (6653393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4df9096884b546264a553ed2aef67263c8c9ebee77e752b92dfe27039c520d`  
		Last Modified: Tue, 21 Oct 2025 21:10:37 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
