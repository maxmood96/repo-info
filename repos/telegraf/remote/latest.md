## `telegraf:latest`

```console
$ docker pull telegraf@sha256:49dbcf977fccc4eb1a0ece3d82b782fde035eaf9a9c50504f885cce42897cd8e
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
$ docker pull telegraf@sha256:f79645d0240b0e7e8d28ad7f6d0a7a21c408033ec1cc13fc7f475636f7d5bf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163445043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3bfbe4006c53d3dd7547eaba528445155ff825901c246ad6988318386fd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd1a615af2df22f2b15f5ad5cb2f173a13e164ce9f01bcd751a557d3e4acb2`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 18.9 MB (18947918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73752d9a19ef19ab378a03d151489ff46b7504b598354287b7af1a7026474f7`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7b40e7109ff62a6cd577ccb8c67c850ea2eabc0b6554dae89a3a5edf511803`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 70.9 MB (70888320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b47b69e9123c04c769e565d6cbe88d5e8d16926891d6c84f21eb573d9e7bdf`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:340795b11e4b687c0b80db6c7ac286e30165342ad8d22cfb3e3878a4c4043d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6111778aad66ee2131172053cd72afa9d883063ad67d709a6c00d6c691cbb76c`

```dockerfile
```

-	Layers:
	-	`sha256:39c9cc119205ae45e26963ea62bfa9636de7cf8ad630bc193c22cd6dec8a2900`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 6.4 MB (6428233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243163876f5c67d58f3511c40b96decffae025e1deb3f824ad9c899ef0d70c42`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eb1362b86487c58cc3eedcecc930c1d2ea707d1a54f23f2e86adde234de1fc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfbd47e80505ab0beaf46701ea3812258575cadeab78102ef5f6d9b3334ca4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145c46c1134675dd81d7f150a5956cd0534991b8712626affe84fdbc492d4e0`  
		Last Modified: Fri, 18 Oct 2024 02:16:51 GMT  
		Size: 17.7 MB (17724833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007f1d0a3dbb40db976a12849fd9dd9414e474b07b7a6ba8f34d999f06745782`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69e3400482d857fc0fefdc3094f1780d3786c7bf40eb6d242715378395ddbf9`  
		Last Modified: Fri, 18 Oct 2024 02:18:42 GMT  
		Size: 65.7 MB (65660236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51dd83ebd073d1f6f0b7104313b22e4d288a94654f56d973e8eca63b665f5e1`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:33cab6f8f48c594b57a6f17dd41e8e621373f2a6425a91a9c38f5ad1c447f774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1488cb71875a1522166dd1d8854f3b8d58d4f45b08fb3233ecc348d37994ed`

```dockerfile
```

-	Layers:
	-	`sha256:8d733c2db9cad610b0062cde762936efd02cbf1328906e4d9ba359e7abc3e052`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 6.4 MB (6404504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462a53325ce6a198b081809a76cbd910d4218603fb675e197ae7e1f3fb2d0d39`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 14.8 KB (14752 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bb4045f74b9acc3bc69b21af3f3e56c183b2d23aeabad3a23d03115d3d742228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99a4b0c4e80c0bbd5969e030260fd33530331849090df3ffdf2898ea6c625eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a729e136449584637961d6c36466fd4de00cf1bd3c42a5b0ef2cc649a9935`  
		Last Modified: Thu, 17 Oct 2024 21:22:22 GMT  
		Size: 18.9 MB (18870637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc475b03394d09612cdb1d4d2c146bff32385599b122b5d5385fd6e1011322c`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d962aeb4af62e2815d8d098f34c65fdfb61d4d0ae402093d32d0e23cecba4e`  
		Last Modified: Thu, 17 Oct 2024 21:23:47 GMT  
		Size: 63.9 MB (63904347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eb623d0a674f3fb99e0c2851fd3509f2f430558ae529e97a20e207a1caa715`  
		Last Modified: Thu, 17 Oct 2024 21:23:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0a4ca1cb89f457657faf440c2fcf2b12847d46f2eba5bec565f507a2c3ea6ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a351f1db952bb14500d8c1a31af9b318ba419c93a6f414068a2204f121e114`

```dockerfile
```

-	Layers:
	-	`sha256:4557c62bc087ec90e827f830c44e03677c3539d5cc8282a3b6d2f3b467e33e6a`  
		Last Modified: Thu, 17 Oct 2024 21:23:46 GMT  
		Size: 6.4 MB (6409790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bf8c96856c70b3c79754ffabccac33d2977d04279aa5bc4d399cb904fc71285`  
		Last Modified: Thu, 17 Oct 2024 21:23:45 GMT  
		Size: 14.8 KB (14780 bytes)  
		MIME: application/vnd.in-toto+json
