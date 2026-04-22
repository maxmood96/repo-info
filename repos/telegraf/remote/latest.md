## `telegraf:latest`

```console
$ docker pull telegraf@sha256:88eb354ac9926d70791b70558d69644b527b3c7e6f02c2af9165038a3e306a6d
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
$ docker pull telegraf@sha256:3278cab4b3ba80a90e2de385a9855dd4e3500c891025a982e1c5dc51f57f1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174547969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e6dfa7b8ce8f5cc1bd36dafe5ee923713b0fc0ddf123ecd310ce4102ee7aaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:16:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:16:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 05:16:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 05:16:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:16:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdaa6f91c9ba4895ddb392aae95bc41fff1e0597f39b3d6a96b67500de023c`  
		Last Modified: Wed, 22 Apr 2026 05:16:34 GMT  
		Size: 18.9 MB (18944330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77e8a73df98439739f415dd132afbece308e0c5d694a0d38a765e4904aa86e`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40d61eeb10ad19b0c1deeee0bcba32c309264ff42136064ada8798f128faa09`  
		Last Modified: Wed, 22 Apr 2026 05:16:36 GMT  
		Size: 83.1 MB (83067082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a33f3a5d60285ac12d5a9eeeab3f92064752300d3b3a75fcd16b90c8b3e322`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:6293af4bad25705a78b1dc84924547003b1863bcc59474e92bbb515d97ae81da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930334ea18d85ba05593bd839e27a887835513365d5cc0f56b5d8a88e95e131a`

```dockerfile
```

-	Layers:
	-	`sha256:e81c19a14633e8727bea8c55b5630657691a6ea57998e353bd2edd623e295b91`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 6.7 MB (6676117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193bd5147cc76d0e7667bc71ddaeafcd0990ea9a4498d2c42eb4e96b0f015b2c`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9c34d13f45a6fe087e8b762d8fefb174b7aedfe46c8b0f066e2fd3a26a4671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160829606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb782f542da35921cd1cd23f40605441990d7123ba00a1df765769174ca50bef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 04:04:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 04:04:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:04:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742f40fc9d5bb902bd77ee1549e0c0815816441cf37052058bb32ebee0e18ec`  
		Last Modified: Wed, 22 Apr 2026 04:04:59 GMT  
		Size: 17.7 MB (17699933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8726f263804a6205f42456a2db18b58eac1f997dee87aa0a54c367d66366f8b8`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c472b4f00d8e1d0623d3c9cdb5bbb924e15ca10c0492d280a152d76a43b60`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 77.0 MB (76969998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e12d49f366146ec8630190da0ccf729e6d970e44bce60ea1f65670cdf0544b9`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f5b5648c87d352bde9bd712fed1e666268fa06c582a8dae4f4f75df99b9d89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccf4b491558cbb21acf76bd1a280a051f07701fbc5bc25832ba635179b1b8f2`

```dockerfile
```

-	Layers:
	-	`sha256:20aafae970bae744f4f1f865dbe6e13bc42e74c41734b18e4a4966153deb05da`  
		Last Modified: Wed, 22 Apr 2026 04:04:59 GMT  
		Size: 6.7 MB (6670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e54bf1037c1b5f317d6bf5f0f522625bd3bed553c47c6add94800551e6a8ff`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:94cec1265657b661cf97bed460c428b3760f4156637de5aa38a65ba122c58e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164951045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6a01e1373825d7bc9d85167c7cf3756f6a7a8663b4b179cd56060e46bcd1be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 02:45:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 02:45:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:45:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264e018336b4afedc4c6c2eae7bf9c8a47abd9fcd044978c11423a06a0060e9c`  
		Last Modified: Wed, 22 Apr 2026 02:45:57 GMT  
		Size: 18.9 MB (18885932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd0995bf7067d49c403e08c32d6c48e03e0bd82e49dfe6a56c4aea107d1f3`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3480a92102a815f6264a05a3fb0fe8a7527dbf5cad4c772d9b545419c269efc`  
		Last Modified: Wed, 22 Apr 2026 02:45:58 GMT  
		Size: 74.1 MB (74076940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af3e5712b7dc9b1067f4eaf53e0f4f025fd2d8539da812449e82435813fdfe`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:70c949d885543e44567741db3a8d9a0f516fb74bb6bc6cf05f9ecf44b5d8442f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6691656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2373511b792dfa6a7ab716e4c6bb0327dd901936bc09ad1ec0386112fbc11b`

```dockerfile
```

-	Layers:
	-	`sha256:66a9f60f79c0bf2a3b62657d4b02928990c0488b1be62a2f37ed52d90174b1f5`  
		Last Modified: Wed, 22 Apr 2026 02:45:57 GMT  
		Size: 6.7 MB (6676805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72499d4039655c2e504c2149df5089645e647802f887758d92f2e86aa81ae813`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
