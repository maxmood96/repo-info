## `telegraf:latest`

```console
$ docker pull telegraf@sha256:7708b428bc575bba389229c19635063936f50b52ad76144303b69b9652ebd07b
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
$ docker pull telegraf@sha256:999669639f67a3aceed2ed2284cafb7bb30e3021904c12d0ec2b543460b547d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172253336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e776b51c62e154f30f558107be59135307c2feaa4497fb03d3e706f964d05a42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 22:12:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 22:12:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Feb 2026 22:12:38 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:12:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Feb 2026 22:12:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:12:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:12:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:12:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31cdf6320f3522e05712bf44784543fd7171040b14dd5c9f6b7acf56a2b070d`  
		Last Modified: Mon, 23 Feb 2026 22:12:57 GMT  
		Size: 18.9 MB (18944502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33141c354ea874f3a4eb068b780d3a42f1d56edeb2b804df9e5f621d6a32efc`  
		Last Modified: Mon, 23 Feb 2026 22:12:56 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e513782ef5aab9764d13a69a05271384b51f2a80901227b87c4628ee43db55d`  
		Last Modified: Mon, 23 Feb 2026 22:12:59 GMT  
		Size: 80.8 MB (80783207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3eb03c1d0303fe3c220ec5f25fab3e038acdf3be4388c5e7336979e18eef4c`  
		Last Modified: Mon, 23 Feb 2026 22:12:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:a40ff796862aeff83fdbba9b16c2ad3d52959566634208631412dfd9b27ae8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c20eed7e6f9e7acc8c8c36396b40b7e58c1b34ec35a75a9aefe357a8edfd36`

```dockerfile
```

-	Layers:
	-	`sha256:3c336c0e2c9da9f4813f1f60c9deb2677fccbbce0a7ad69bfd7b6e20748251de`  
		Last Modified: Mon, 23 Feb 2026 22:12:57 GMT  
		Size: 6.7 MB (6667260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc696e678d93c0307eed1877fef811c78c62f2ce45415b37f331191192ae06d0`  
		Last Modified: Mon, 23 Feb 2026 22:12:57 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ec2bfdaa2b7b54b2e923ef4eed5601da7c0bb54afc3937302f4e846cc5fa580c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158463795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86d1e8f5b24828595fd38eaa76675478d7ea79f85505bf4466d67059d267a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 22:10:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 22:10:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Feb 2026 22:10:43 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:10:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Feb 2026 22:10:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:10:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:10:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:10:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913ba3c14b6362700b8fc523f5f6163f69684a9f184204be11cb0a38e3fcc80b`  
		Last Modified: Mon, 23 Feb 2026 22:11:01 GMT  
		Size: 17.7 MB (17699892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32944774181a89d85568b35da0e4f44dbd6ca1c91d947ae528b25b1889364f3d`  
		Last Modified: Mon, 23 Feb 2026 22:11:00 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6537677519ab0fdee25cb2b781cb8789056b9c330d1ee16c3fcd7157b4579990`  
		Last Modified: Mon, 23 Feb 2026 22:11:03 GMT  
		Size: 74.6 MB (74617431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c1bc9b33d3f2887a06eeb2570c66f2157cf61ac39cd4d25202d7b91e4d20d`  
		Last Modified: Mon, 23 Feb 2026 22:11:00 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:93d9dbef44fe8162b93acc55f384873a97b4eb207afb816aac2fc88ec0cd0570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20bcc80d031b67e0811f0c728796852be1b37bb3a131cebb1cad9cfb03c0513`

```dockerfile
```

-	Layers:
	-	`sha256:2cb14b7305594c96e1dbdba2fafca4351b400ac4355beb08196259e5a456dc4e`  
		Last Modified: Mon, 23 Feb 2026 22:11:01 GMT  
		Size: 6.7 MB (6661865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:562437fbd8efc014ea2f371e5c2761d30e60d5a053acf2dcad8e43eb8f8b731e`  
		Last Modified: Mon, 23 Feb 2026 22:11:00 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:abe6962a108d472db4db5b75fc12475d4d22da8a5c8f42d381e4283ee5c1c405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163033336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437cf3ce801132e41e5158e4e1abee6c617cd7fe5402a8d1bbde4e515c1f2319`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 22:11:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 22:11:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Feb 2026 22:11:36 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:11:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Feb 2026 22:11:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:11:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:11:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:11:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fef6e107ea76dc9f54b9018c26353126f79fff911c442fd8aea6b8524471954`  
		Last Modified: Mon, 23 Feb 2026 22:11:53 GMT  
		Size: 18.9 MB (18885831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e189aa8854839bdd9741b85fab7b0ed2c5a5a3629b30de38b54da853e52e449d`  
		Last Modified: Mon, 23 Feb 2026 22:11:53 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9748929b955a6d209afe4faccd4f9f19f403342e0bbbbf7d56f036eb68bf2450`  
		Last Modified: Mon, 23 Feb 2026 22:11:55 GMT  
		Size: 72.2 MB (72171013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227d9002d3b54040e79c668c8e4760f683936909edd70d9d7a444c03bc5525e7`  
		Last Modified: Mon, 23 Feb 2026 22:11:53 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:5afad2f518bc66e5a44d4a609bf23ee31280d1331a0cc8b7e82e14b434a8ffb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6103253df4f243f36109577d6a46a7da7a7ead7462a274c4971f2a16c159d4`

```dockerfile
```

-	Layers:
	-	`sha256:722634ae8c2ce093109b6a280d54d06a12808281bd7b1e8d26356060951b23c1`  
		Last Modified: Mon, 23 Feb 2026 22:11:53 GMT  
		Size: 6.7 MB (6667948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f35f18c31ae4c3a8c596a398d159b082e4dde8c8a6c06debf73c5619ac1ce6`  
		Last Modified: Mon, 23 Feb 2026 22:11:52 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
