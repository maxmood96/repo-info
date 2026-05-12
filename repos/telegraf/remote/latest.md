## `telegraf:latest`

```console
$ docker pull telegraf@sha256:cf7f3e5c0cd7b1ee5ab69b707fe7b30e3b969c2b940f087cc84debe92ce0aae8
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
$ docker pull telegraf@sha256:80f0262f1764d7220207e02d4f39e2e4746a57836865f95339121c2f5d4b9319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (174991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c60b6e1594923a92cb94407321531d19377b3f65ff3d0f2b9a13618f5234b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc401cab11768d2b73aa0f36b0d76831b9aa4c7a568fdf9be0fa309112ef4fd4`  
		Last Modified: Mon, 11 May 2026 23:54:06 GMT  
		Size: 18.9 MB (18944282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf251f55455c38e3f15bed7a3f75b426f1815c5d0dce73125a3617fc770a62`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a720032e9b8bdb47e8f616671f2022496c72cf16644ad344541cf9d2b135a92`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 83.5 MB (83511119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c19c791a0de19bd603e238311b3d1fa63543a036ff1f69d222c7e7b1dce41fd`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:55cbed9339d919070e63e8ec47800577b2df280770b0f6afc723190d297a3a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6689294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4934a5127878b8d5da77a4ceb933d0c592f8332e1119e4d02ebd3205ad434146`

```dockerfile
```

-	Layers:
	-	`sha256:febb6e9adddc67a1c7ad1bc75bfbf4884cc6b32992f68ebd4f2cb60a9ed0a7e5`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 6.7 MB (6674565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab5e4877b539a3bedcb6961e259913239cd77f99ba352bf3cb774d5fb4da89c`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a04f5de1f41fdc580bf27c29e7cf392a389198156eb0988abd4c83e25e675fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161287558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1bdce67fbf4f45c1907d2d9a913aa2da7bdcaf53273d0ed34099497664685f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:50 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6eba3c782b7cc747ee4a809321eebf18d8982c91ea59720226b56cac299608`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 17.7 MB (17699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618dd9f2c5aa795ad17b5c76403cd1d2f28c2a8a4be35ef9a3c963e71104631`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b47fa8118f4e1b53b666dfc2d985df74424cff2482f6f7ce3268ec8b3ef5da`  
		Last Modified: Mon, 11 May 2026 23:54:09 GMT  
		Size: 77.4 MB (77427909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fe4d37f249d0b62a594b3eb04746408285e8763e0b846fd7031d7e3c0a71c`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7fd0f946cee5b67fc708d89eb1fbc208bdca91e28630d0f28b10bb390255286b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6683997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a209fb2471636227dac7b3f894e7f4b4d265e322ed71c06322fdff32ba436ce6`

```dockerfile
```

-	Layers:
	-	`sha256:67b856fdec15003642b567bbde1db8736a5c99300c58a08bcb65be0cc7b37850`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 6.7 MB (6669170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0572bfd71e1532ea0d65afa82546864d446b3780babb902b2406fdbd37b18a56`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9d5ad52e5e2b07a326e5cd0f0f064566b413335ca5704768cc173da61ffe0a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165350749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba33f42f3b75c6f86298a199f6f46fa4d3c7ef629cbd4350ee11c43dd66f849b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:49 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814a8bda2fbfc42c158410ad33c204312964d366ad654eccf35597219b49b9ad`  
		Last Modified: Mon, 11 May 2026 23:54:09 GMT  
		Size: 18.9 MB (18885813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618dd9f2c5aa795ad17b5c76403cd1d2f28c2a8a4be35ef9a3c963e71104631`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472f805f5e0ffc4e1ed052f46b773ec7e7c39887926a10953189f7aafdd2b9a3`  
		Last Modified: Mon, 11 May 2026 23:54:10 GMT  
		Size: 74.5 MB (74476737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fe4d37f249d0b62a594b3eb04746408285e8763e0b846fd7031d7e3c0a71c`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec75681b0736c5a8ba960e031f6573f031b7a4f5a97da4eccc6905c7b57ff184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9a392223a61f98d69639a2ee694a7221d184761b44ccf470ed0f28654f58ec`

```dockerfile
```

-	Layers:
	-	`sha256:3128e488344cda446d4255fc7a4a85691d278f03fc0fdf963b0312b35d3b4153`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 6.7 MB (6675253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a9a55247bffe2184c7f32a22162b27d6839dc2affe61be40888960239dde1e`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
