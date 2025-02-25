## `telegraf:latest`

```console
$ docker pull telegraf@sha256:087783af38ad58b701da6c2a53fd5319f0d299702a115f7604ad7a5badaf929a
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
$ docker pull telegraf@sha256:0e20b846d9899ae9b86688ab34e6d3e836319fe78f596145f84f3a1afd84493a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167818964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e77c194d1304c21f28786a430d64b5dbe1565f4a5792397e387353fc91c3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c658cdde06a1e65ba1002194efed4848e35e244409acc7c78e8d97bebf7786`  
		Last Modified: Tue, 25 Feb 2025 03:19:40 GMT  
		Size: 18.9 MB (18948049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa4b4f5cf5b6e6b5b8ae49862efd932205ab78607f281fc3831bf9a7f763352`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d24e2103cf750df19a4c11f9a8702f311cbf91cfa860d6dcf72b0533b14ef`  
		Last Modified: Tue, 25 Feb 2025 03:19:42 GMT  
		Size: 76.3 MB (76333879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3c2c4ed2937ed31f842f4519a3f724492b8b379a9bb7822b44fa1ac6c0f02c`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e9854eb40d6cbf9a7fa892556d5beaaecefd1593bee1e0821437dd553cae3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6453920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796b73d5653c4020e8556be51509120215cb3c8dbb2af2dd4e03d8ca48f5e832`

```dockerfile
```

-	Layers:
	-	`sha256:0e03a257cfbc0c29d4649a2a13e2b3978a231681694a4792e24a6428ded91791`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 6.4 MB (6439148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed0280b00b4bbc5082a718e72f7e6536118286d27b9737c472b2004e70236399`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:631c670d815298bf1f01e9fc14a70a9c7bd7df381413c2f6f8cf9703f88c6acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154403882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b7d15c4334993a82be810f026fa39135482da26066349e5f69993fa3cb98a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad85eae4eeefe28382b2b6ac022363abf12720aad417db847747f7cedc24e4f`  
		Last Modified: Tue, 11 Feb 2025 01:30:27 GMT  
		Size: 70.5 MB (70531910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78465c33b061c5ae7946dbbaa605f1f867b1eb067fa2855063e286ac831242`  
		Last Modified: Tue, 11 Feb 2025 01:30:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:93190e99f59af7e4b86571b6be0b588840260f7a057d24c488ebe065c5db4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aed9440d4d8fa5f34ec0f4f034d2ada4b4415c95fce9276d64b5270762d6db`

```dockerfile
```

-	Layers:
	-	`sha256:bea2ca2705b89231972f0f25adccd1a433f3d0bfd15e8e4e3fd71d4068b5d196`  
		Last Modified: Tue, 11 Feb 2025 01:30:25 GMT  
		Size: 6.4 MB (6434542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2665fc8fe71fcacebb712ffb1f8fa69073fee2a894fa79dcd10281dff936e306`  
		Last Modified: Tue, 11 Feb 2025 01:30:25 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a52f579be8879ab811a43023136bc80273b068ac5d2428c1bcca5b6c1a5ec1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159823353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0482f0c34431d6c2adf636e0bd282ee7d8a092e21958e1fbe916a1991e994`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bcf63b4ff6fa63b5e72af00ad5db4255c5aaa3771526590165a03d9354c295`  
		Last Modified: Tue, 25 Feb 2025 14:22:58 GMT  
		Size: 18.9 MB (18870670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5919f122039cdb24f3f65e32f513ff925f97caf4c5d1490e990644265653e9ca`  
		Last Modified: Tue, 25 Feb 2025 14:22:57 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c98c553b9355d2ae2a9b13642e4537218cc56887c0fb73e5bacf3150a83e86`  
		Last Modified: Tue, 25 Feb 2025 14:23:34 GMT  
		Size: 69.0 MB (69044004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3de81cdd34603beef4431e7737c1077c744885449f1935092b907a3b285c090`  
		Last Modified: Tue, 25 Feb 2025 14:23:32 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:1ee5c1d2c42525a7aa170adec5fff57bbfdeb0a967a5fd31bd8033769f6bd28a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28ab34ce15bf6f1bd512ff4c5399e6f1c0a0f69eb405d7cc1f470ec437383d2`

```dockerfile
```

-	Layers:
	-	`sha256:c7f2bc34f6d09f29b4ca841a71d0c558ef7158682ba7670f2b44aaa23bfd0cc1`  
		Last Modified: Tue, 25 Feb 2025 14:23:32 GMT  
		Size: 6.4 MB (6439836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72e238be180e670a58d0e1608bf092cf8a0e862a96f6f2db23a274efb90b97f`  
		Last Modified: Tue, 25 Feb 2025 14:23:31 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
