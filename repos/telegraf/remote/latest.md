## `telegraf:latest`

```console
$ docker pull telegraf@sha256:597f83e62cf0bd5944452cd8920ee2e118609cb4a856cba63723a6f0b71a3043
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
$ docker pull telegraf@sha256:9974d7ace8b151642478d6a23d43e1323f8bc201f914d7262751f495bdbab9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3124c4971b8c7f0b45f88505d3653a7bfd7d7dde0d7fedb9099add1c9e72f53b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 19:00:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 17 Nov 2025 19:00:07 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 17 Nov 2025 19:00:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8991d306ad7c356c103a6fb4479f141847774044f4500d4bc1984f05a7036`  
		Last Modified: Mon, 17 Nov 2025 19:10:41 GMT  
		Size: 18.9 MB (18942624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a646dc383e0b1e995623739f80989c7e07b2ebb646f8d14e8af30fb473f0084`  
		Last Modified: Mon, 17 Nov 2025 19:00:37 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a015e97829b72bf5ec52087002a3c31c7a705e96b740c29b39e31b29d27e42cb`  
		Last Modified: Mon, 17 Nov 2025 19:10:43 GMT  
		Size: 80.5 MB (80473486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9168a33d43584ddd6b154cdf77899d4b8e095ff7a6075fbdd755d54b64b5a797`  
		Last Modified: Mon, 17 Nov 2025 19:00:37 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:2ddb3562a246b222c5c07d9aa3e6472f2490fc744dce69af3bc6b7002edb343f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2877ac02fd501e17a238844af3980623269fc971625d08fdc681eddf65ebcbba`

```dockerfile
```

-	Layers:
	-	`sha256:e23053edfa534e0e07cc315923ccefb06c78c99d3f0118f4de6c332f653664ee`  
		Last Modified: Mon, 17 Nov 2025 19:10:27 GMT  
		Size: 6.7 MB (6653548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f77971dda3fb77d14645b96a9065a037eed8eb7bba3e52d2ef9602bf12e6c4`  
		Last Modified: Mon, 17 Nov 2025 19:10:28 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b2005056c077e404b83e1bb443e5bc605992d57e68a75601bafbbecb31e17d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157821343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf18f6e4f4745a2538712b4e8c458491788da36f4977412febf68f474150061`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 18:57:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 18:57:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 17 Nov 2025 18:57:16 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 18:57:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 17 Nov 2025 18:57:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 18:57:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 18:57:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 18:57:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f9d1d3f8138586aecdc0e101f85a634b64e2e9d1afa86154ac58a655c426ae`  
		Last Modified: Mon, 17 Nov 2025 18:58:05 GMT  
		Size: 17.7 MB (17722398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b9801187742602fc94e0051f58328a5853b1ca106a2ebda661848a9396b617`  
		Last Modified: Mon, 17 Nov 2025 18:58:04 GMT  
		Size: 3.4 KB (3449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d9ef39a38bafb574dae0e947c79a2c2673844caf8ef673798da1ab53fb5362`  
		Last Modified: Mon, 17 Nov 2025 18:58:12 GMT  
		Size: 74.0 MB (73963557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd226cf2d99fc5ea0a249b6c01943754970b7fa915c882b671c4495eedeff32`  
		Last Modified: Mon, 17 Nov 2025 18:58:04 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb0bc6723692b10be1c8f0d40eb916bd8e95a08fae975b2ffe6d5a9ed4a133f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf24c24893c6354062fc51cc548df2bd3da7c2ac395300171f46f1f810e0e2b`

```dockerfile
```

-	Layers:
	-	`sha256:7b28a4ca0130e48538e7be717e8ea6c65507827200e83c99edbb91f1d412e36b`  
		Last Modified: Mon, 17 Nov 2025 19:10:33 GMT  
		Size: 6.6 MB (6648153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c06326b4027be18cd77d22c8fe14881ea6cfc5d7e12a881692c19b04288b42`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5b5b8eb284241464434ccf8b6d02cfcc677e65bcd0b013a3f0f1a964f33564fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162646893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030b1ffc925a0f415a14691d92ceee18e8f5404da67a7bc49e6d5ae83ac6ef9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 19:02:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 19:02:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae5ce7e4b622031f9b1c1c614e0e02285631337c7645b678af2d0e40de56690`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 18.9 MB (18884546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dca5eec15032cfa8c8f804b178053ab506fcc723480aabdb100f4632b469aed`  
		Last Modified: Mon, 17 Nov 2025 19:02:46 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbb9a4a393b727f736768aa8b76f048e620ba7bde832830ec083e6e1037e418`  
		Last Modified: Mon, 17 Nov 2025 19:02:54 GMT  
		Size: 71.8 MB (71800282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c84a269ccee1195fd5fe133ef0ba2bb666e2f3c58e37dbfd65d52f5cc48f6e6`  
		Last Modified: Mon, 17 Nov 2025 19:02:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:a91d0d1a6372a476d46b84bf2b913730391a041b863bebdeffad6b897f07c0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6669086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381c42b11d8ec32416b27efcaedc2eb1c4d9ce6dc9c72d2968dd29262322e0fd`

```dockerfile
```

-	Layers:
	-	`sha256:09f8b1b2b04169ff4f30cac78e2f8591cc950c38f45d946fe8c6ce5594c22d93`  
		Last Modified: Mon, 17 Nov 2025 19:10:41 GMT  
		Size: 6.7 MB (6654236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a7f37fdb0ca9ed0738fad65397e7129acc46a056cb54054503be46d06891876`  
		Last Modified: Mon, 17 Nov 2025 19:10:42 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json
