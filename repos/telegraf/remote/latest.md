## `telegraf:latest`

```console
$ docker pull telegraf@sha256:062455b2e39324ec791168c4a82ef825936551c62b6e52e61f2ce0683f78b8a6
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
$ docker pull telegraf@sha256:e396e6b0fc235d80c69a2737e6d303c8178034c19d935fa4646cb143b99c22b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154599417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1463988fb9ac4d7f92622e154f20a430349ceb8e9d80ad5c6c7480e42586e3eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
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
	-	`sha256:f76047489d0b2ccdc4598bd413a2f7f8cddf3685229a8c8d2dfea4e28147e471`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 18.9 MB (18948018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c013e6ebce0fe5838f78b11b747a7ae2fffa092cdee0749609bfac6ae129058b`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049270f6c151d3bd1e976b0ca9a6d3aaabe9c2cb5ca253cb53edfb086182ecfb`  
		Last Modified: Tue, 14 May 2024 03:58:26 GMT  
		Size: 62.0 MB (62022501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1cf419edd6c5b8dc261f09c429795709ae8ec676035b9432f2635a6aa7a94a`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:82aaf3de49fedf1eb53867ae333b120a5baebce276115a08001a49cb66e0ec6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6312805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeeb6e6fe095a30e3ff49b6266c69beaa7f85fc9dd7290d1eef8c3bc33da59af`

```dockerfile
```

-	Layers:
	-	`sha256:b2533c5a707801d71bd284a7fabafe70b0371175da6b354e741a5f639fe0f9d7`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 6.3 MB (6297897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d8718e9191bd392eb11b4485e6e87d2741437935af64356b66f9dd76f93338`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 14.9 KB (14908 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b42974d2147951e1891eebf7cde1ed5597982d8bd389f5ed1f814683f546e655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142268061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1542ae530a1a2ff3497adb860e8cdf08ed73d23eb4e30c1208b72c73d5b8369`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c7577918dea746df9c5fbcb51b929d73f1915b3c0e7723a4aad3ca148c343`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 17.7 MB (17724944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b7f4d906aeb5335da996f149e84e5db08b1905e7ceb937cca7a8c9ac360ede`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1702d62770944a6a6088dba2d4c1f99350f12e6de561f4a2c08d3e1aa5020d48`  
		Last Modified: Wed, 01 May 2024 22:13:32 GMT  
		Size: 57.4 MB (57411744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46965f9978bfadf9724ce2d3cae10baafa08d0de0b2ee52a4775ffa2f4eab101`  
		Last Modified: Wed, 01 May 2024 22:13:30 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0fff7c5047b86c2c9bcbb6f021523fce3406e9ff778b675c6a8e01225a0a7330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6307923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df2fc033378f3acbac8f2ba1051996e57a489a90d9400aac223906579d204fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5eed3c367c698de5243e012e512e93bcfb073261fb1c1f1360df30e47f9d627`  
		Last Modified: Wed, 01 May 2024 22:13:31 GMT  
		Size: 6.3 MB (6293259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16eeec4048d39e68a41a306fd267533f6a0a2023c6016075e3b8a046c66407b`  
		Last Modified: Wed, 01 May 2024 22:13:30 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77fc16f95036dec5f73c379d0c0b083133115e496bbb88a12c997eb1f812236c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148491545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ccc7cd3d68e411ff5e323927fa7376edd2b1648d5c01cde611bf7867da8b7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4668ee134c6d27b158f31b1c01b5e92a02ede4c76d4b570eb243b76e7b7567bb`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 18.9 MB (18870222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c26c91634d198f308ee466c4f2be3a59218fcaea48af76c19274245b1725a7`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b65e3ef18a3b059c80d045b010aabe08d82d2c8504bb9b8d1e1cf28bea72b2`  
		Last Modified: Wed, 01 May 2024 22:35:35 GMT  
		Size: 56.4 MB (56418780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad2f9c46f3a11a31992befffc6b5533b6d86ea19882447a48448e2b936ba85`  
		Last Modified: Wed, 01 May 2024 22:35:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:336bbf80fe6a5d81fa90823a3663f5d4c6c6e5dfd4ff920a21fc0aa478942a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459f674c96e863832e3ed1390d07e3512fb7d49e6f01921a45497fba22864859`

```dockerfile
```

-	Layers:
	-	`sha256:ea9fc20d24af05be6bdcb3ece4c941918547a8353f7dc1d6e4b2554b0c58f7c8`  
		Last Modified: Wed, 01 May 2024 22:35:34 GMT  
		Size: 6.3 MB (6298512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43457d5c0f51f13681689d84eb3e643c3585306ba9c420ce87c401c054e78678`  
		Last Modified: Wed, 01 May 2024 22:35:33 GMT  
		Size: 14.6 KB (14584 bytes)  
		MIME: application/vnd.in-toto+json
