## `telegraf:latest`

```console
$ docker pull telegraf@sha256:5455056dddebfa85d7bc8fe724278bd1847e856eb610a0fd2cad829f1afb2838
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
$ docker pull telegraf@sha256:14182b461ba97401a23631904ecc8ce7d4a388b1005a95a91dc090d972d83427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172205272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ae40de51ebdb9c5a0de896ad61df0c8a8ff35da610de7bb7d79434e76c9d80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:15:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:15:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955c1c7e9186ca7bc0e6b217dc58cb859974a31b211d9ee7c66cb3852c4de40`  
		Last Modified: Mon, 08 Dec 2025 21:16:30 GMT  
		Size: 18.9 MB (18942891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea07bea6c4d7b93f73b8efab6d6919fad6cbcafccdf6914e6e889faa645e2744`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 3.4 KB (3449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691acc2c25c38154f83c6dcb07a9f84167e31889f80361c6b198b94d2d7c201e`  
		Last Modified: Mon, 08 Dec 2025 21:16:38 GMT  
		Size: 80.7 MB (80748200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33376e647ead58704e9fd8ee985b8f803cfd401900f089e25cb87896ba4985bd`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:5622219565f39096961784d31e044c8cc4efe6dba0a4d483fb7e6137617fbbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30b3a77d69d09cec4c6fcf9d64ee32de7360028ec0371e16c152ad5cd34b5fc`

```dockerfile
```

-	Layers:
	-	`sha256:96f17ec2f1cd92f64ec27f849115c114bfdb6fb6a9673f9c05db99c5ce9f1caa`  
		Last Modified: Mon, 08 Dec 2025 22:10:31 GMT  
		Size: 6.7 MB (6664397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50832b27b515571cc652e8d8b5b018fdc6b72e290a124102005d08833ff64b1b`  
		Last Modified: Mon, 08 Dec 2025 22:10:32 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c23fbb7392e98dceb10d548d2c667b7e6c78a9d695d5bac0293d60e36de3e513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158440177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb53ab8a14948a52176935ddb53585573f0680f536757440d114e3fff7fc7d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a08dfa69d8ea4e22baa8dc6670d74f3393f85a4b481ff079651c1a1212d96`  
		Last Modified: Mon, 08 Dec 2025 21:15:21 GMT  
		Size: 17.7 MB (17722482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889819377807975d7dc9d21289246cc30df973dba3e5abde28b40968a45b6fb2`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 3.5 KB (3454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4260d0aa9dcde0e457ba2df5abb42f635a157e8603996cfa34d843ea9dbccd83`  
		Last Modified: Mon, 08 Dec 2025 21:15:36 GMT  
		Size: 74.6 MB (74582804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c55b9f9b296a78c3075c04cef854755a94ab309f3e43951a10ce3019e0440`  
		Last Modified: Mon, 08 Dec 2025 21:15:20 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0064ac2489bb0a9d84883effe97fb927693f3146382010e1462202bdf1d5759f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8825565d8ad43bb8bfd021103a694b9138178e324adeea9c2ea585fc922e27e`

```dockerfile
```

-	Layers:
	-	`sha256:2851b9a398db71ff6720c8a7f2517dc3cef2aca78b1f2ad266885a972f0b90de`  
		Last Modified: Mon, 08 Dec 2025 22:10:38 GMT  
		Size: 6.7 MB (6659002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00a822f8e172bd707d3b440c51b5b536acc3c22247e132f3fa466f069f4e9c99`  
		Last Modified: Mon, 08 Dec 2025 22:10:39 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:11b23df6f74f8b39ffc8c0df9258f4b4d6aebb4e1d6ff3f46b156da0801acb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162859621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbb8f084f2788441c7235812ffa98d6c92378cf68c50e1ffe6d30d843dde2d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e886215090eba2379645b59d5ea77586aec42fe7f5f8191a814687af5b35a83`  
		Last Modified: Mon, 08 Dec 2025 21:15:27 GMT  
		Size: 18.9 MB (18884530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd780df0c406cf70d83e3bee3770d1fef950cbedb50e2eb4e4f52b3b8192524`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79997b3be7f3731b6ea1ec5a68d53816fa82b35a088caca4ce42021c4e7499`  
		Last Modified: Mon, 08 Dec 2025 21:15:28 GMT  
		Size: 72.0 MB (72013557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec078996978b3045acb60aa5d6f4ce8d586c40a69e44c096f2af1d023dfa4e9`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:d983eaf8761c6c0c47692f24beb3663531f9edce27b91320263fe2bedda23d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d149aad78becbc65b063b18d56d9417c3a8b1823d01a8e9538d2bcad42402dd8`

```dockerfile
```

-	Layers:
	-	`sha256:9c63a57edc0ea0221917161838d74d3cde5194efc5166ef3086cc4e666dd2a54`  
		Last Modified: Mon, 08 Dec 2025 22:10:45 GMT  
		Size: 6.7 MB (6665085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13983d5fc1624bdf36b6c803cea632a7ac27e1ef203af03ec652dbbb82bd95b9`  
		Last Modified: Mon, 08 Dec 2025 22:10:46 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
