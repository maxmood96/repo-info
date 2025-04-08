## `telegraf:latest`

```console
$ docker pull telegraf@sha256:fe39c7c8d549f203dc77289dfc8f8c2deb068771b4b6bb218efcd1465a674169
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
$ docker pull telegraf@sha256:a6529f1674ac6472055f3653f174b4bfb1ebbc679336423abc55a0d81494318c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169093197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8dffeadec1a0ec9cfd5b70ab080f4be0ff5eadba60830601f6badc0fa4dccb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENV TELEGRAF_VERSION=1.34.1
# Mon, 24 Mar 2025 21:11:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 24 Mar 2025 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 21:11:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fe954ce5919c12b553770e9ba6840267def89afb8b5f591814083a26713627`  
		Last Modified: Tue, 08 Apr 2025 02:22:44 GMT  
		Size: 18.9 MB (18947920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fa92b41efe1779065d49a715458d5376f1953bb4dcf3b5864d6f88c578241d`  
		Last Modified: Tue, 08 Apr 2025 02:22:44 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c1e41860e4a9610f604a9e2bfb58d78687ca246912d674abae876e287182be`  
		Last Modified: Tue, 08 Apr 2025 02:22:46 GMT  
		Size: 77.6 MB (77641242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18cb26af6fbe2b3b7ab7d79d867042f25be927e86503611debebf1537de6397`  
		Last Modified: Tue, 08 Apr 2025 02:22:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:3e740e38be5b1dbaebd24488ddc7fc92aa3763e924b5dffd1c23faf2b16f0134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233ca1f7be1396d7ac76ffb78c44c1c973e874ac2cb5936911d48c83e246d7e8`

```dockerfile
```

-	Layers:
	-	`sha256:8c5561108d86f92e02d45f86b3f3ab86e696ac5d479dce5515c36fb2f6d389d3`  
		Last Modified: Tue, 08 Apr 2025 02:22:44 GMT  
		Size: 6.4 MB (6443822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca95f19217b653ece5dafc237894322a27ab5e67d65cced5560c96a585d4f186`  
		Last Modified: Tue, 08 Apr 2025 02:22:44 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0a7a1e55d518723def906fd0834cd897e9b912aab20806825c4949ffb5747fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155270864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed39a8d67bf875600a5cc3967ad9587e585756e6195b0cd856be8f4ae1a9784f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENV TELEGRAF_VERSION=1.34.1
# Mon, 24 Mar 2025 21:11:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 24 Mar 2025 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 21:11:50 GMT
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
	-	`sha256:9e11f748f8843220ee99150dbf6645bd257137a85e4e5224e5875835e7cf2913`  
		Last Modified: Mon, 24 Mar 2025 22:16:07 GMT  
		Size: 71.4 MB (71446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d4009c969cac18c12f5b6ebfd9eb9402340db60b84696e24e9f7fd8b72eb3b`  
		Last Modified: Mon, 24 Mar 2025 22:16:05 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:b2dea19ea92b334c91a5b5696c12afa65afb643bb1871b8c6503e7061994ab01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7010633e8e6a8aedafcab7e89979067a747c9389ba6b3329fe3a59d031fb2afb`

```dockerfile
```

-	Layers:
	-	`sha256:86173b6a614642512c4ee3669af536d1663ad0574dc6e1aa35d2ba50f9d5761d`  
		Last Modified: Mon, 24 Mar 2025 22:16:06 GMT  
		Size: 6.4 MB (6437869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec36f57190bea1a3a60b0e0da390ba16146d4e2beccd8ef47a07201b47a86be2`  
		Last Modified: Mon, 24 Mar 2025 22:16:05 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:27a5e132bb4575944dbde38ce490071e94456e6d6f4b51c4dfd2d66348411d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160638831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c9ea2fca32f1791b8cef021f4e0d2b20ca9f7d9d90a058ab5d8817a6f2d385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENV TELEGRAF_VERSION=1.34.1
# Mon, 24 Mar 2025 21:11:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 24 Mar 2025 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 21:11:50 GMT
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
	-	`sha256:ed865a39579b173825dd0cfff1917afd509ac0875f9f03d3ef1b51cbf68c121b`  
		Last Modified: Mon, 24 Mar 2025 22:15:55 GMT  
		Size: 18.9 MB (18870916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020bd02679a0b988668b77e8c2cce184625b388227d7cc8a9471a74748c1a43e`  
		Last Modified: Mon, 24 Mar 2025 22:15:53 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47818dbc3aefa09dcff39d10c971e7fd77c7311ff35d450c4c3babafeae7f0e0`  
		Last Modified: Mon, 24 Mar 2025 22:15:56 GMT  
		Size: 69.9 MB (69916302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d54ed1c36e692e1aa6606e8faa68ecb05a8d6f5d8157e11ad0b5256e21f2219`  
		Last Modified: Mon, 24 Mar 2025 22:15:54 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f6639cb9f2759081e338ddc7e13aab87751c5c07bd61563eeccd56c727fa4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1ad74b97981f60918a03fe02df317ea9311ba930f4212232626a1c5e04c242`

```dockerfile
```

-	Layers:
	-	`sha256:317d6af4cae20c2146212c6d0a392080e69b012eb41826cf711194f2e549a3ce`  
		Last Modified: Mon, 24 Mar 2025 22:15:54 GMT  
		Size: 6.4 MB (6443952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed7b13cd2b0f46529fb5c4ab1ec95c91ecd75f1e736e65a76885b1ce4021011`  
		Last Modified: Mon, 24 Mar 2025 22:15:54 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
