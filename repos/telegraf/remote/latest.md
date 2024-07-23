## `telegraf:latest`

```console
$ docker pull telegraf@sha256:f5d66098b7dbc6e30087a74e43a690a3a16c05c6db70c712d6a69abf3f9b3a15
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
$ docker pull telegraf@sha256:6ac005eb5a03fbe6471ded5f1f77c416f67b2e6ad0a873c393c9fefdace5566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158826722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9540c29ec541b4b0c36d46b9c6b9ceeb72d6e112a66ff07ba42c3b1b4641072e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jul 2024 16:07:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.31.2
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270a1743a173eac58352af906ad709abad8d87dd4a5a3375d0c713d33ebce7d6`  
		Last Modified: Tue, 23 Jul 2024 07:28:36 GMT  
		Size: 18.9 MB (18947972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb8e96ea945e762dc0f8ab841b85f578f1fff33c50e9591ecda79e2c2afd3ea`  
		Last Modified: Tue, 23 Jul 2024 07:28:35 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c801770fb0aa41d846b6ab6c7c24be176e9fea72016fa9a9f0ac49dfe236c`  
		Last Modified: Tue, 23 Jul 2024 07:28:36 GMT  
		Size: 66.3 MB (66271481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50bf92d7cf1bbf45e3d57aa93ca970a2c82cdbb84a53bde7776271f7737a2c3`  
		Last Modified: Tue, 23 Jul 2024 07:28:35 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:406ff0a065d55f3889e8c89ce6597f81bc9cee18c7a1245c94e5b407e2da5dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdfc0803662fa7f554a2944a025bde7b6b87c7b16c2425715c0e1feaf8318bc`

```dockerfile
```

-	Layers:
	-	`sha256:ca16dcd60482e32000400c7df284ae1523934a1dc21375ff7d9699cd59bb3796`  
		Last Modified: Tue, 23 Jul 2024 07:28:36 GMT  
		Size: 6.4 MB (6398662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5888e45038b7a9443a23ff9527e5dfd51d5b54ee66edfdc906be41b9a9f69f01`  
		Last Modified: Tue, 23 Jul 2024 07:28:35 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:bd326c1e04da02a6334b2adc11a33126fb5f4bca543e27fb7f6e835937dd7529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146430538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6c497ad4bd877235dc727f34b836a9683c7066e9b23174518c7505c40f0810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a987fd3254b4eb8a2e6cc7206b9d5eac3e938a9d3c13d8fa167031b4fbcce`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 17.7 MB (17724841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17cfe5d83da74d5e8c4d81b008e6599fc7cca1105639345e4bf236669c7f0c5`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb5b65e557f72b22f833c43955f3c8d36093fd4040e5d8d436bc2f39dd8362a`  
		Last Modified: Wed, 03 Jul 2024 01:36:38 GMT  
		Size: 61.6 MB (61601152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f5ed5bd1d96e3bf9e9b6f47eaf1e1aa50042560ddc6f546da60292553a2f16`  
		Last Modified: Wed, 03 Jul 2024 01:36:35 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:e031f34a1bc0b974683b355de0553a9bc75a572a724cdc37cb87839c016959a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6315093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d317ad92eb5361752a0696f2725b1f92deff7bdddfb49f36188c03b20af44d`

```dockerfile
```

-	Layers:
	-	`sha256:1aab98ed50ba77997063ac8e4d303152b55a27f70a4465de6fdbf5fa1404f018`  
		Last Modified: Wed, 03 Jul 2024 01:36:36 GMT  
		Size: 6.3 MB (6300379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1b16159e9459b5b279a5f297fc73228d4d21f3d2996504fdb2f28a9eeb1c55`  
		Last Modified: Wed, 03 Jul 2024 01:36:35 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9df7de5c3c95b0f72771ffa58f2b9a5a5dcf22b41b63a6b9fb244244a06e3249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152336093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fce67cb8fa54d34a54c6266529978c8db1a3d91fb2a8f72cc4ad46e963d103`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa4258ace16a879b6bae48191a62329ef9150aaf9ac97497e6d6c0f3d622aa`  
		Last Modified: Wed, 03 Jul 2024 00:51:44 GMT  
		Size: 18.9 MB (18870342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c902d4b3d360929e7f2bfb7aebbb19eb7c0bd8f515cf202c7fe68e2315b58`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53711602d3ab9a60d8d35c9202bbe4620c8c8fd1888fb16601d4bf36e311690b`  
		Last Modified: Wed, 03 Jul 2024 00:52:55 GMT  
		Size: 60.3 MB (60283753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78887db2826f45f52baafab97c61e63c1124243fd6cae85e2f8c3a06853036b3`  
		Last Modified: Wed, 03 Jul 2024 00:52:53 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e7d3e64ffa05e5ff13896af64e5aaf547d82c4b22de2a8b5630b0e6470f196f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6321250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f69bceb31f7804c7610329c5a403aba38aa8a6e6b8c4aeb879381d81b7bbeba`

```dockerfile
```

-	Layers:
	-	`sha256:152e5903a51b12964d1ec93c4d2aa0b4929a87744964442b58e3d753aa892a59`  
		Last Modified: Wed, 03 Jul 2024 00:52:54 GMT  
		Size: 6.3 MB (6306319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3e466a2111dd26c94480a8dc228e399e4ddfd66f64147958a1783efa147799`  
		Last Modified: Wed, 03 Jul 2024 00:52:53 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json
