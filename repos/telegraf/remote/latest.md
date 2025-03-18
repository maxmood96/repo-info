## `telegraf:latest`

```console
$ docker pull telegraf@sha256:9eb6b87162c5687ef1d1f239b632902e4ae75c16075047f3766c7323b94fbcc3
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
$ docker pull telegraf@sha256:ef6b3b8263255d73794171372e0fdee2c11292e2b4df701145dfa6fbc75197d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169071117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed0097b6683c8d436e7481c8b603e6d00e0ee8e90b4d20284dd815c5a381ab2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654601e6c8b9fd8ca45760fedcddd51c744ff38b7524df1f98de4de9b5a4e11c`  
		Last Modified: Tue, 18 Mar 2025 00:23:09 GMT  
		Size: 18.9 MB (18947973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d29b84bbdd29c8bbc1fb894fce6b9a4e116f94816fb5b244a97875d1bb75b6`  
		Last Modified: Tue, 18 Mar 2025 00:23:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af9b081a02229146c28d3b238aaa1c10cad10b7d8dc3240757aa492f9f1dc4`  
		Last Modified: Tue, 18 Mar 2025 00:23:10 GMT  
		Size: 77.6 MB (77641771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842502b303c5ddf715806f04cfe00f9491a931c07ff7f8a8983afdb1d2be47ab`  
		Last Modified: Tue, 18 Mar 2025 00:23:09 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:dab13c33eacbad01583a16f6b0e8eedb0aa34b5e140d67d29ed553d7a396cae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5466f028c1743b4bdb1f3d55d520ad800f852d6b963cb43334341b28d6843edb`

```dockerfile
```

-	Layers:
	-	`sha256:1f7f21a06b4faa1926d56f5014fc4bea582b5bec59c2831afc5e31dcc251a279`  
		Last Modified: Tue, 18 Mar 2025 00:23:09 GMT  
		Size: 6.4 MB (6444063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57ec286e8679879319ad679ef75e8dc7cddd864e3371943ac5f3455f9465d110`  
		Last Modified: Tue, 18 Mar 2025 00:23:09 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d3cae8d1e1bf2c5d0aa7b865ebbbee705d56a989b1f9ba436634ac1affbb5b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155203599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb911ecb619dab94312ef5a91a5b4e4a9193b25099a0be33b94077ac2194c26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476ac467ed0a1d2a02a8351335caff580de24d82e97725278191fefdc5c89db8`  
		Last Modified: Tue, 18 Mar 2025 11:42:11 GMT  
		Size: 17.7 MB (17725471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8966b6d6ce8b823f96c30a42b0b9d81058b9be60afa6484ad21f65fb820d73`  
		Last Modified: Tue, 18 Mar 2025 11:42:10 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7eefef1e74e08589b50f799515ffcdc7d1ebfa2fc54b8e981b6cd5203f38ee`  
		Last Modified: Tue, 18 Mar 2025 11:42:13 GMT  
		Size: 71.4 MB (71379698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b442d75b8a5417b1ad7e7e5a8df3ede68142eb9c8b5b0dfdb08b182ae13659f9`  
		Last Modified: Tue, 18 Mar 2025 11:42:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:dfef892c15a70de7041c2d16a29e9cf37ca29581fce2aede5af1fcb9cfc374ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145f1340a72ff6e0f5c5bacb6e05ab96922d639da98c50006edc1b616196ca6`

```dockerfile
```

-	Layers:
	-	`sha256:0bef027ac5663a9d07a16c5e23ebde64ea53da9a379ee2ed6e18b3f720c30dba`  
		Last Modified: Tue, 18 Mar 2025 11:42:11 GMT  
		Size: 6.4 MB (6439475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dbada6ef92b5e8d104393c25f7581369b10e18dd6edbab1df3c48e0c0a12101`  
		Last Modified: Tue, 18 Mar 2025 11:42:10 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:936daaf62851eccdbaae1c8b86900e5aed13965855bf05e659bb4b0b0341cddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160616024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba037a031349e5d91cad09c58afd86454b75428bb596975ff37ed9bb74c8e1f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d030badc415b7a0972d2510275c7330ae4a5f46e82ed002b5579bd096e29091a`  
		Last Modified: Tue, 18 Mar 2025 11:20:37 GMT  
		Size: 18.9 MB (18870869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e751cf7278176340daa39a68eb80d2e29b813af79d3f2e6e0c6589cf57b32f2`  
		Last Modified: Tue, 18 Mar 2025 11:20:36 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a44f4a73635c5844c53aa7d43d67a11479566c32b2fc098e2776a36eddf2b9f`  
		Last Modified: Tue, 18 Mar 2025 11:20:39 GMT  
		Size: 69.9 MB (69893540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff124dd71549369afe1503af0af65e7a28d7e742aa0fc301bc42c60786e9f914`  
		Last Modified: Tue, 18 Mar 2025 11:20:36 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:db352abefbf7fba29eb88ec22e98166632cc8957439a11f6903536f5f7bea55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b292782a7e55acc487c9322c86d9ca6107cc106e064e275c88c40b771735cda5`

```dockerfile
```

-	Layers:
	-	`sha256:2a47b211da3c8d63aadb4f95882eb369a43e12b6d9e4c3f88b514729c99bb734`  
		Last Modified: Tue, 18 Mar 2025 11:20:37 GMT  
		Size: 6.4 MB (6444751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:567ceac78f30634375f8620300316360b81a5838057149a3a8a61cddedc60fe7`  
		Last Modified: Tue, 18 Mar 2025 11:20:36 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json
