## `telegraf:latest`

```console
$ docker pull telegraf@sha256:cb10bf03a9f426cf9e34dfb9d4c3bf2b0a7b2cc66b5a32267423ce69a8f96ac1
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
$ docker pull telegraf@sha256:0bf8d0b836337c94ec66c11f36bf35b653348fc4d274f242c7c49df70a7b6ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158781425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ef5932dbb288c90648457ca93ec01caded5034ec8bd2cca94d4e8b8667869`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
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
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73640a629d5c024f9dfe1e45997e798ee73d8a1610b0f3b8323574909a371251`  
		Last Modified: Tue, 02 Jul 2024 03:32:15 GMT  
		Size: 18.9 MB (18947959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b734f825ca42c8b2531d5b7bff4a2fd773b28e939e01ba10cd88aba8b1d5923`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5592f5a587d7f8eedb6976959e4f68eced16e31fd88eadca308608811f4f2ee5`  
		Last Modified: Tue, 02 Jul 2024 03:32:15 GMT  
		Size: 66.2 MB (66227197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1345e4c69b07d7c081836490c21d7fdcf540c9048e4dd30fc6cbb845c5c9e0a`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:acb0bd848143d98105741c38a6e2c59d0374115be8f9da3c9133fd7d86110f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d34bd18c3254b1f26fe2d3a73e22e781ba64cde20b65d21cbddcb43fac5ff1`

```dockerfile
```

-	Layers:
	-	`sha256:64ff97c343edd9924cbb0d64971baecadd617383c57598cc79313feb2f8abd2e`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 6.3 MB (6304363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e60e4cc25bb1bf81857c3e626e050e6bbef9703b8b409cb67cc933378595b25`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:30be19e0ea0c39c533845067d8e5085278b1422fe897e88f977b5d10364a7df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146457213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c180ed2b573319b06441fa08c9122e5d084ca472d9dcdb6b91ccb9c528b2eba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
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
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10defc1b331e76bb57a1726cdf7fb34a4c4e149a9632c966701894b65c612b34`  
		Last Modified: Mon, 01 Jul 2024 23:58:09 GMT  
		Size: 17.7 MB (17724836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c4f8cd77635772cbc86bd84c093606c9d526494186c59685bb3268057d1a04`  
		Last Modified: Mon, 01 Jul 2024 23:58:08 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cff616f47b98dcbd36515a47cf1e179a5bda9c6188d3872ddf663faaf44f93`  
		Last Modified: Mon, 01 Jul 2024 23:58:10 GMT  
		Size: 61.6 MB (61601163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265327d5390af47d9e61068df4aa2047f0795010b5f0312af00c0e0da5ffaba8`  
		Last Modified: Mon, 01 Jul 2024 23:58:08 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:e2810f32105acc1c17772fe4ec33080502f54410bd001ebf019a1409d22bb431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6315870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7916d35e548905783a15452f7b5d57ce319107950039075f46b7ed0c892fddbf`

```dockerfile
```

-	Layers:
	-	`sha256:bda93dfe7c23bc482bcefa82d8e3226f1961f2fb1d3896a16cc928a19667a287`  
		Last Modified: Mon, 01 Jul 2024 23:58:09 GMT  
		Size: 6.3 MB (6301157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65baa1e57173b0507921969b3a0dbd8b245818f40ac4c8fa3c15001620ee9587`  
		Last Modified: Mon, 01 Jul 2024 23:58:08 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f20456299ac6a26ffabb48ed4e23bb40215a436f68b3d0b4d29f23dd7626af23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152356827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d77bc7af9d2b2e7d0e170bde67e3efb192ae8f8823f91097e2c903d9b576adf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
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
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa1453c4bc86d5c7ff50f1e4a18771df129d9318f557d75166e01ea4c99d53`  
		Last Modified: Mon, 01 Jul 2024 23:58:48 GMT  
		Size: 18.9 MB (18870720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e8103745f532d7315c1107cdef774b9da9d7856993aa480c22bd9203412b5a`  
		Last Modified: Mon, 01 Jul 2024 23:58:48 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453c203cb04eac48ab305228ec3c53d563cc6f30fe0ab0d7096ea85ae088b88c`  
		Last Modified: Mon, 01 Jul 2024 23:58:50 GMT  
		Size: 60.3 MB (60283727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f2fe625d938f8fdac3e55a5334895f96f73153440fc5474d7a3ab6dbc7b4bc`  
		Last Modified: Mon, 01 Jul 2024 23:58:48 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:6b4f227a2773ede90124b41ae76987680e3cd71d134e24655d366cb319d9a463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6322028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a10d617149eeafa250c9782471fbe28f905de4b416e53ed99843d82441d467`

```dockerfile
```

-	Layers:
	-	`sha256:41aa7182c3c0dfb60dfefcabb3b166428e594ab1e69485ecb2a4bbbce5171b44`  
		Last Modified: Mon, 01 Jul 2024 23:58:48 GMT  
		Size: 6.3 MB (6307097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfbe3b1438161c1a55fbf1a3fdaa47148548cd9ea66210a01526bb55abca614`  
		Last Modified: Mon, 01 Jul 2024 23:58:48 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json
