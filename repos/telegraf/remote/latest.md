## `telegraf:latest`

```console
$ docker pull telegraf@sha256:61e27ef3daa5b4843101742e09737a6e8eb0849b64388f0dcfe40f866eee8710
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
$ docker pull telegraf@sha256:b1a51ec96e9f223fac9779fb8ca3bf432bf40f5aa4f9fdc097bc596e5a670569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155289847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a45e16fb8aa871926a41b7c6a1424ff05270084188c9747b97a24d9236c793`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86bafb7d50d5e687e5ba6eb8b1b69311347f27f1a43178cc6a9de872819b032`  
		Last Modified: Tue, 08 Apr 2025 19:35:58 GMT  
		Size: 17.7 MB (17725468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6ab320bc74c4e39664c1424558c1fce932673ccb4f2b099b68dc06884861b2`  
		Last Modified: Tue, 08 Apr 2025 19:35:57 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82e09fdc51aeeb1eebdef213ac32a77354f93755cbf25372b8343ea3659eb63`  
		Last Modified: Tue, 08 Apr 2025 19:37:39 GMT  
		Size: 71.4 MB (71446959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a465892242cbe94781105218065736bba3219a09aad44f908f92c41b719256`  
		Last Modified: Tue, 08 Apr 2025 19:37:36 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:01d161d1e2bde1f856acde5792fb1ffd0d01fdf107800acf172cae4339e9ebe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6453293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfd3ce6b4c64327f24d476478b8612d5f5890acf4d8cc342b2353ceb2af7eff`

```dockerfile
```

-	Layers:
	-	`sha256:71179b766e776c8a8e46dc0374303c4b1bcab174834924b9309422de3a5eb436`  
		Last Modified: Tue, 08 Apr 2025 19:37:36 GMT  
		Size: 6.4 MB (6438427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1288fc6c7ef8c9a615826393d515bc28700a520d4b998c9688ea4deddabc943`  
		Last Modified: Tue, 08 Apr 2025 19:37:36 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1d24ebd995fa172d7e21ebc94db3c3d8391c226e94697a602a4deeb3dc836c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160661383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851409ef06fe9da6b8da44399ef9becccf5ef46f6ad545902b7fdf4ec0fcf16c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173a1eedffe27442f0cb28acb2719eb2174e1d758d462f023379f4538ec3d3f0`  
		Last Modified: Tue, 08 Apr 2025 14:58:30 GMT  
		Size: 18.9 MB (18870871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e690eaefd0984bef7c0b3aafca716d73da0812c1a0edd65297b132507ab35b20`  
		Last Modified: Tue, 08 Apr 2025 14:58:29 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411690eab11bc70f80ef2ea55911eb332765b934c0b8d9efec4396ff7e36b402`  
		Last Modified: Tue, 08 Apr 2025 14:59:34 GMT  
		Size: 69.9 MB (69916295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80e78ae721fc604ef10ae35d627530f459d76b9fb409e3ff3419317e2ec9b1`  
		Last Modified: Tue, 08 Apr 2025 14:59:31 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d84e80d78a02ae4940983d4de0bf1e3b913cff09a6799bc12052f7609cce22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d17e485f392495e783a32b9b65eb19cf624ec6d23882c6107b1255c0b610fd`

```dockerfile
```

-	Layers:
	-	`sha256:92c1e270dcd901d444ae0abcf5fe76cc2aff032c501e86e984a3161eb87e8ac6`  
		Last Modified: Tue, 08 Apr 2025 14:59:32 GMT  
		Size: 6.4 MB (6444510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16de3780fc97bcd44ff50beee8137b1ee217946710969bd40f1e4d4b32a91fff`  
		Last Modified: Tue, 08 Apr 2025 14:59:31 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
