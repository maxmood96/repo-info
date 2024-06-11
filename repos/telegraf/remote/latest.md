## `telegraf:latest`

```console
$ docker pull telegraf@sha256:be0e7c04e4876560322eec497d44fbec1003a793d9f6abfd389b673fce92b8e4
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
$ docker pull telegraf@sha256:44dc8b1f371f400ed282951f09c77e717d4629b38d295bcf37adafb95cceb243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb33388867057e3193fe2d3768501720a7ad9f2acc4b43078eb2cc22e5147a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba02c6ae7fe3311dc53f8cc7ef5044386dc1b913664583f7a6f270ba83be5853`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 18.9 MB (18947865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc44775bd6481d3e78c7e2e12361e98e4227c8e9e463f1d93f83589d1b9095`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3672b395fed0d417ceeff47f3839a16e0b978aeb7d1bc0f228f9cccd67cdd5c`  
		Last Modified: Mon, 10 Jun 2024 22:33:02 GMT  
		Size: 65.1 MB (65089317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd204feb12d817fec8d8730699b552d5490725be1121fbb508ff0e5ebeb61ef`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:f0b28b3a379a88b32fa46e49985d81b74033cd04affcb5b89e8cd23f311508f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4454cd70cb0be5c2706a0d29111ad45bc776dc5e19963365e0bcb97f89b80f1`

```dockerfile
```

-	Layers:
	-	`sha256:237de469e10f3b5b75580715df66063159386618e49010e34d7ca85b0071963d`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 6.3 MB (6303812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d28a42ccc99d982a61ba3d837e377bc45c9762559146c164c950eb904af1ce`  
		Last Modified: Mon, 10 Jun 2024 22:32:59 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0937b1a222978be919cb00df24cdcfa62d8a100dccab0ab3776ccfba19e31a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143068661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2f8ba5cd8962f90e947f7fe1309436728ed13ef21c5fb8bf4dab976ef3b3cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:08:35 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Tue, 14 May 2024 01:08:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:13:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901b8b18d82e5b57b89385ec062d1674265344d73cca05bba989b96a6cf4f07a`  
		Last Modified: Wed, 15 May 2024 08:08:19 GMT  
		Size: 17.7 MB (17724872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6537ab1b98b6a7364bac3f994ad624855097573d29bfa741f0a5f24eaffe2bc`  
		Last Modified: Wed, 15 May 2024 08:08:18 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f4a236ed04d98e4dbbd6c88b87392bd54e369cfbb75ba5afcace4dbb33b6ef`  
		Last Modified: Tue, 21 May 2024 18:08:27 GMT  
		Size: 58.2 MB (58212744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8eaaf18c8e5e6fb3073500e84a83e0722dc3b3231c64d24a578c283338d60c`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ea09a00736aecf132e6b185eabe3f050148ea41c066980dd8d9cc03768abd799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6309812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419e20c776b8b40e3ad5056c424586ebfdd0254d17d6d87c07cc05f3bf274422`

```dockerfile
```

-	Layers:
	-	`sha256:be92ac005ea43268c72221d35410b3ffe5cda8c51a0f7fb2d095fc2a8259e1c6`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 6.3 MB (6295147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6d8ab8fcfcde216a402b8bedfe934dd5adae59f9659864fff791d9ef974c86`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d062d9a32a4d87ea479fa7887bcb7813c9139badfdda83620cbaf1317f0d885b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149196386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9e574432b44679b03199dc4767cc26b2d1f2c504cf5053af7a32a97cf038c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:13:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c90cc4c220f2efc01fd1f87a403a247f61d1030f562e906930332d905ebdb`  
		Last Modified: Wed, 15 May 2024 15:06:57 GMT  
		Size: 18.9 MB (18870680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23862d11452a5b51a68997e785996fd1e75da32dd2d37041a0da1bf5f6d58f9`  
		Last Modified: Wed, 15 May 2024 15:06:56 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77927e413fc545578865de64349d36cc081fb9cddad7d367cbe6603e44b48cc`  
		Last Modified: Tue, 21 May 2024 19:35:30 GMT  
		Size: 57.1 MB (57123300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbc39928b2eb309725c009a597946c56c6a462adc4a0bdd10fea3ba4a245ff7`  
		Last Modified: Tue, 21 May 2024 19:35:27 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:fee17afc9e9dc2f01e041248c868b8a0c5f0296b9ebd44adf0759fa569c8061f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cbf4f25a66722c5fa564a3fbe175bffaba0e2911c66085c299f720eacaf700`

```dockerfile
```

-	Layers:
	-	`sha256:4a45036b1e98c4f63e4867f33d7068bc8635061614a4648ec2e3033520a0650d`  
		Last Modified: Tue, 21 May 2024 19:35:28 GMT  
		Size: 6.3 MB (6300400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0c4cd04de694e67f0f823819d8428380c279bf3cd7fd56c726e6a8dde2f06e3`  
		Last Modified: Tue, 21 May 2024 19:35:27 GMT  
		Size: 14.6 KB (14585 bytes)  
		MIME: application/vnd.in-toto+json
