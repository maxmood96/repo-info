<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.35`](#telegraf135)
-	[`telegraf:1.35-alpine`](#telegraf135-alpine)
-	[`telegraf:1.35.4`](#telegraf1354)
-	[`telegraf:1.35.4-alpine`](#telegraf1354-alpine)
-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.4`](#telegraf1364)
-	[`telegraf:1.36.4-alpine`](#telegraf1364-alpine)
-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.1`](#telegraf1371)
-	[`telegraf:1.37.1-alpine`](#telegraf1371-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:c592d8dd9022f32d18d30fd39399217d66ef634adc3f652014243782e697d8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35` - linux; amd64

```console
$ docker pull telegraf@sha256:98b80e565cfa2f281bfec49e0da0dee5cedae03cc74d69b968116a3d5ca7a768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171039275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fb107bd7bf2c5b674e75411e9052b21b5cd074af79ef40c497b91aab170bcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 13 Jan 2026 04:14:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:14:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:15 GMT  
		Size: 18.9 MB (18944358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91406583fd9d6f02fe192491d186b903784d752b175a5ab23fc8277f257dd37`  
		Last Modified: Tue, 13 Jan 2026 04:15:08 GMT  
		Size: 79.6 MB (79570735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24651fcb5ba6fe63163acd54a779fa445ff0d75ce831f9784fd259830d92a71a`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:4c2ccceb0e6a181ec42ffc23e0dfea0bd47967ccf2f44dcf5fd519f9fa1d26d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d772ccc069272cc8d9717741ea30a21482495375f054f65a47132904f28f63`

```dockerfile
```

-	Layers:
	-	`sha256:921f30471e438107b48281d3c7062eea888b5210b113c7f31bed8b96ebe23c8a`  
		Last Modified: Tue, 13 Jan 2026 07:12:51 GMT  
		Size: 6.6 MB (6647803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e4cff05cea2bb7107fc84f5ab4534cea98df7eb2e163032b3a16c1db5d1369`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7347d2646b5f45a5b6db7d2b7c55f451e7526f21db079268cb89a21234473a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157136721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4f780e1d08a95afe0c1ccde1f4edab8e9ad4c4d90c5229d2ca280d66e31ce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 13 Jan 2026 04:42:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:42:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:42:22 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d545d030870d426bc777e5c833ddeec574860b248b830258001d7e907fbfb5f`  
		Last Modified: Tue, 13 Jan 2026 04:42:49 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e726832fe5a5c92dd689aff89da387dfd545c947c6233589660b3f3669420dbe`  
		Last Modified: Tue, 13 Jan 2026 04:42:43 GMT  
		Size: 73.3 MB (73290783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8923ad93aec8a70e3c96191fd9846e9633e80aae6c51dd10c2866dd2e41e3c`  
		Last Modified: Tue, 13 Jan 2026 04:42:48 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:ca81be3c6b218fa35d12d97a8afdac2e00a14f3ae09836bee37dc03f1604d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f210c3da4b3d7f35eb6937c3e6fd0a0d350a352d3fbfbc68052fb7064af3d37`

```dockerfile
```

-	Layers:
	-	`sha256:aeb9c29c52169ce56a0b4b8a8bd3cf6c5eb6cc5579a30450e14f7711aa008eab`  
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 6.6 MB (6642400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f487977cbba703ae72c1086a6ed26eed4dad58ec385f7c01cfb323d9c71b19`  
		Last Modified: Tue, 13 Jan 2026 07:12:58 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e3372d4c700a9ebd4e1104c182cc6983b618bed9b0e4c04ad549eab6fc2cf338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162941865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa92e161d7f61958a5c7d747e7bb2dc129f708a3f59e68c6354cb42fb11093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 13 Jan 2026 04:14:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:14:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d901276e8d660c9c3643003d1099eedd64836cf2c857706c853224234cd680`  
		Last Modified: Tue, 13 Jan 2026 04:17:12 GMT  
		Size: 18.9 MB (18885851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2359d97ce7c58015c1632ff80cc75cd613494d5d320ef65198fecd11fac54c`  
		Last Modified: Tue, 13 Jan 2026 04:17:14 GMT  
		Size: 72.1 MB (72079434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023ebc8490433522006f58bc45c4e91657ec0506159e767c125e0a6ca111963d`  
		Last Modified: Tue, 13 Jan 2026 04:15:24 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:d15d2f6355cc034223bc2e664b3ab0800743072b016bcef675421a8533f22343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6663016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25854892285991f24785e766509bc19479dc58d0f7eaab3a377719031c1aef0`

```dockerfile
```

-	Layers:
	-	`sha256:1e2f3daa33e7064fbcd7fa8b76b080f0453d972d03b86d30279cff72bc3ec432`  
		Last Modified: Tue, 13 Jan 2026 07:13:04 GMT  
		Size: 6.6 MB (6648479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4ad23d8a413616ad24fc4267913b6977d019eeea06d3f3c7cec66fc6892cbf`  
		Last Modified: Tue, 13 Jan 2026 07:13:05 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Wed, 08 Oct 2025 23:21:27 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Mon, 08 Dec 2025 01:56:53 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Wed, 08 Oct 2025 23:21:28 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Fri, 12 Dec 2025 13:09:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Mon, 08 Dec 2025 11:40:46 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Wed, 08 Oct 2025 22:09:59 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Wed, 08 Oct 2025 22:09:56 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:c592d8dd9022f32d18d30fd39399217d66ef634adc3f652014243782e697d8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4` - linux; amd64

```console
$ docker pull telegraf@sha256:98b80e565cfa2f281bfec49e0da0dee5cedae03cc74d69b968116a3d5ca7a768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171039275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fb107bd7bf2c5b674e75411e9052b21b5cd074af79ef40c497b91aab170bcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 13 Jan 2026 04:14:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:14:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:15 GMT  
		Size: 18.9 MB (18944358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91406583fd9d6f02fe192491d186b903784d752b175a5ab23fc8277f257dd37`  
		Last Modified: Tue, 13 Jan 2026 04:15:08 GMT  
		Size: 79.6 MB (79570735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24651fcb5ba6fe63163acd54a779fa445ff0d75ce831f9784fd259830d92a71a`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:4c2ccceb0e6a181ec42ffc23e0dfea0bd47967ccf2f44dcf5fd519f9fa1d26d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d772ccc069272cc8d9717741ea30a21482495375f054f65a47132904f28f63`

```dockerfile
```

-	Layers:
	-	`sha256:921f30471e438107b48281d3c7062eea888b5210b113c7f31bed8b96ebe23c8a`  
		Last Modified: Tue, 13 Jan 2026 07:12:51 GMT  
		Size: 6.6 MB (6647803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e4cff05cea2bb7107fc84f5ab4534cea98df7eb2e163032b3a16c1db5d1369`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7347d2646b5f45a5b6db7d2b7c55f451e7526f21db079268cb89a21234473a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157136721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4f780e1d08a95afe0c1ccde1f4edab8e9ad4c4d90c5229d2ca280d66e31ce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 13 Jan 2026 04:42:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:42:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:42:22 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d545d030870d426bc777e5c833ddeec574860b248b830258001d7e907fbfb5f`  
		Last Modified: Tue, 13 Jan 2026 04:42:49 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e726832fe5a5c92dd689aff89da387dfd545c947c6233589660b3f3669420dbe`  
		Last Modified: Tue, 13 Jan 2026 04:42:43 GMT  
		Size: 73.3 MB (73290783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8923ad93aec8a70e3c96191fd9846e9633e80aae6c51dd10c2866dd2e41e3c`  
		Last Modified: Tue, 13 Jan 2026 04:42:48 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:ca81be3c6b218fa35d12d97a8afdac2e00a14f3ae09836bee37dc03f1604d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f210c3da4b3d7f35eb6937c3e6fd0a0d350a352d3fbfbc68052fb7064af3d37`

```dockerfile
```

-	Layers:
	-	`sha256:aeb9c29c52169ce56a0b4b8a8bd3cf6c5eb6cc5579a30450e14f7711aa008eab`  
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 6.6 MB (6642400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f487977cbba703ae72c1086a6ed26eed4dad58ec385f7c01cfb323d9c71b19`  
		Last Modified: Tue, 13 Jan 2026 07:12:58 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e3372d4c700a9ebd4e1104c182cc6983b618bed9b0e4c04ad549eab6fc2cf338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162941865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa92e161d7f61958a5c7d747e7bb2dc129f708a3f59e68c6354cb42fb11093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 13 Jan 2026 04:14:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:14:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d901276e8d660c9c3643003d1099eedd64836cf2c857706c853224234cd680`  
		Last Modified: Tue, 13 Jan 2026 04:17:12 GMT  
		Size: 18.9 MB (18885851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2359d97ce7c58015c1632ff80cc75cd613494d5d320ef65198fecd11fac54c`  
		Last Modified: Tue, 13 Jan 2026 04:17:14 GMT  
		Size: 72.1 MB (72079434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023ebc8490433522006f58bc45c4e91657ec0506159e767c125e0a6ca111963d`  
		Last Modified: Tue, 13 Jan 2026 04:15:24 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:d15d2f6355cc034223bc2e664b3ab0800743072b016bcef675421a8533f22343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6663016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25854892285991f24785e766509bc19479dc58d0f7eaab3a377719031c1aef0`

```dockerfile
```

-	Layers:
	-	`sha256:1e2f3daa33e7064fbcd7fa8b76b080f0453d972d03b86d30279cff72bc3ec432`  
		Last Modified: Tue, 13 Jan 2026 07:13:04 GMT  
		Size: 6.6 MB (6648479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4ad23d8a413616ad24fc4267913b6977d019eeea06d3f3c7cec66fc6892cbf`  
		Last Modified: Tue, 13 Jan 2026 07:13:05 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Wed, 08 Oct 2025 23:21:27 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Mon, 08 Dec 2025 01:56:53 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Wed, 08 Oct 2025 23:21:28 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Fri, 12 Dec 2025 13:09:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Mon, 08 Dec 2025 11:40:46 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Wed, 08 Oct 2025 22:09:59 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Wed, 08 Oct 2025 22:09:56 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:c06e2be89a443a2a9d1473814bc4da865e80681ec04f6586fac6644d87d8ae52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36` - linux; amd64

```console
$ docker pull telegraf@sha256:db59b39ab25fd3e4ab7dca2ca8ec4feb91fcfe42c22a8873a5f16636b7b6c4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171942158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c523420ba64adc7fae226d0a1e21753c31eda992ac47967d1b426b5a56fea2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:15:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:15:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:15:04 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 13 Jan 2026 04:15:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:15:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:15:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:15:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50c0d3c5c84f10d1ac2b95e1051abebdbfdc15952bd3e34f82f52ccf0a43e79`  
		Last Modified: Tue, 13 Jan 2026 04:15:23 GMT  
		Size: 18.9 MB (18944438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5190e11dfa902fc0e7b00491041ae2491d045eaf965c3caf1e137268b24a00a`  
		Last Modified: Tue, 13 Jan 2026 04:15:31 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a69654e2ff4e8a54881fef6c442c931ca21dbe768fd2c0514e4792a6db81ea`  
		Last Modified: Tue, 13 Jan 2026 04:15:39 GMT  
		Size: 80.5 MB (80473538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ba7f86dfedd6cc722fc54431ddaeb41939b733a71ee996b3a24d893480995c`  
		Last Modified: Tue, 13 Jan 2026 04:15:31 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:ebd78c1c43b96056747d23091998d6b50a6d18721f5086fbb30bef6d5bc752de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06bf75a22d9d21d440d066cdf6ca01843a4e711980a9193047a9dce13053bdd`

```dockerfile
```

-	Layers:
	-	`sha256:ea7da93b9da477995c22bdc3a8e7cb02206689d350547efb9b9c1248fb406dea`  
		Last Modified: Tue, 13 Jan 2026 04:15:22 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f585faec3e0224f9c1440f17a3ca3263dbfc0fc5846900efd2b8f3768be87747`  
		Last Modified: Tue, 13 Jan 2026 07:13:06 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:55191d404c1e659a7991d3fc66fe17db0700db049e9ef527a48abc49c2164852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157809564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee52b4f7d026fcff09727aacc9fbb46d51f03fbf65bde1ac3a7634a65efc39d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 13 Jan 2026 04:43:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d545d030870d426bc777e5c833ddeec574860b248b830258001d7e907fbfb5f`  
		Last Modified: Tue, 13 Jan 2026 04:42:49 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3260264734f11a0dcf2c688e6b709c967bfbe661975d9620e42eedf009712d`  
		Last Modified: Tue, 13 Jan 2026 04:43:44 GMT  
		Size: 74.0 MB (73963627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31439ca9ab7543fb88a1c0663ac62b7650fe5289524a5808103d51482d333336`  
		Last Modified: Tue, 13 Jan 2026 04:43:27 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:f73fb5631c018efc8c33c79cab881f3bd4e914c16865b14206777b1e3c4e3f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f41fd4ef82359cffad0da19e077e9d1193b1d6d22b2485bf008208f10376774`

```dockerfile
```

-	Layers:
	-	`sha256:97ba1da3e9ec828f3aaf3930e06277f76cd0ccc27fabadf3381c724b461aaf89`  
		Last Modified: Tue, 13 Jan 2026 07:13:12 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a2a55a05b62dc316ccc44feb478292e528f3362b0debb2aaf523d42653b3df`  
		Last Modified: Tue, 13 Jan 2026 07:13:13 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:84c8e10910f255e60c176ba0a0f30b400616ac93ca3edfa9f8227e7c0ed96fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162662662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543953a3f2321265df54b334c16aa6c2fe706cfc80cc60ce48ca4155ba9414f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:16:12 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 13 Jan 2026 04:16:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:16:12 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:16:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:16:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:16:12 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdbccbaf6a168145824d1651dbd7bc7faac38ee214625f5254dd4ba9ead0bda`  
		Last Modified: Tue, 13 Jan 2026 04:16:30 GMT  
		Size: 18.9 MB (18885794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843e0b344a4e5351f09818b295ac69324493def6f22025377d20e3c48ece0ead`  
		Last Modified: Tue, 13 Jan 2026 04:16:29 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc471d4d4e54147d425df5f41fce09a21689fa62c1d37e05acdb637857f8b6`  
		Last Modified: Tue, 13 Jan 2026 04:16:44 GMT  
		Size: 71.8 MB (71800302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceac2ee0ef56101139e946f40b0b2b638560545fa3e79b6cae94f3eb48a2c7e`  
		Last Modified: Tue, 13 Jan 2026 04:16:38 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:bff5e5ce8f6cf610d484bf76ece253fabb3ddb3d72328323656b05bb7fe571c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cec4f699b0d21d66ff3e493aa657f4f50350dd414df54567b07a1605294bc2e`

```dockerfile
```

-	Layers:
	-	`sha256:41a15faea4f2bf19478b93a8c2c8afdfd69450b630d282c4b3e7c0f127911b78`  
		Last Modified: Tue, 13 Jan 2026 07:13:50 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f73686bfc571b066a9e6a7d4bd7e36247d13672bfc9539e3765389d88c59f7`  
		Last Modified: Tue, 13 Jan 2026 07:13:51 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Fri, 16 Jan 2026 19:05:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:26 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Fri, 16 Jan 2026 22:00:56 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:23 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Tue, 20 Jan 2026 12:36:13 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Tue, 20 Jan 2026 12:36:13 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Fri, 16 Jan 2026 22:00:50 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Fri, 16 Jan 2026 22:00:51 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Fri, 16 Jan 2026 22:00:53 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Fri, 16 Jan 2026 22:00:50 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:02:40 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:02:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:c06e2be89a443a2a9d1473814bc4da865e80681ec04f6586fac6644d87d8ae52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4` - linux; amd64

```console
$ docker pull telegraf@sha256:db59b39ab25fd3e4ab7dca2ca8ec4feb91fcfe42c22a8873a5f16636b7b6c4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171942158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c523420ba64adc7fae226d0a1e21753c31eda992ac47967d1b426b5a56fea2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:15:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:15:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:15:04 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 13 Jan 2026 04:15:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:15:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:15:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:15:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50c0d3c5c84f10d1ac2b95e1051abebdbfdc15952bd3e34f82f52ccf0a43e79`  
		Last Modified: Tue, 13 Jan 2026 04:15:23 GMT  
		Size: 18.9 MB (18944438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5190e11dfa902fc0e7b00491041ae2491d045eaf965c3caf1e137268b24a00a`  
		Last Modified: Tue, 13 Jan 2026 04:15:31 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a69654e2ff4e8a54881fef6c442c931ca21dbe768fd2c0514e4792a6db81ea`  
		Last Modified: Tue, 13 Jan 2026 04:15:39 GMT  
		Size: 80.5 MB (80473538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ba7f86dfedd6cc722fc54431ddaeb41939b733a71ee996b3a24d893480995c`  
		Last Modified: Tue, 13 Jan 2026 04:15:31 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:ebd78c1c43b96056747d23091998d6b50a6d18721f5086fbb30bef6d5bc752de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06bf75a22d9d21d440d066cdf6ca01843a4e711980a9193047a9dce13053bdd`

```dockerfile
```

-	Layers:
	-	`sha256:ea7da93b9da477995c22bdc3a8e7cb02206689d350547efb9b9c1248fb406dea`  
		Last Modified: Tue, 13 Jan 2026 04:15:22 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f585faec3e0224f9c1440f17a3ca3263dbfc0fc5846900efd2b8f3768be87747`  
		Last Modified: Tue, 13 Jan 2026 07:13:06 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:55191d404c1e659a7991d3fc66fe17db0700db049e9ef527a48abc49c2164852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157809564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee52b4f7d026fcff09727aacc9fbb46d51f03fbf65bde1ac3a7634a65efc39d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 13 Jan 2026 04:43:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d545d030870d426bc777e5c833ddeec574860b248b830258001d7e907fbfb5f`  
		Last Modified: Tue, 13 Jan 2026 04:42:49 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3260264734f11a0dcf2c688e6b709c967bfbe661975d9620e42eedf009712d`  
		Last Modified: Tue, 13 Jan 2026 04:43:44 GMT  
		Size: 74.0 MB (73963627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31439ca9ab7543fb88a1c0663ac62b7650fe5289524a5808103d51482d333336`  
		Last Modified: Tue, 13 Jan 2026 04:43:27 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:f73fb5631c018efc8c33c79cab881f3bd4e914c16865b14206777b1e3c4e3f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f41fd4ef82359cffad0da19e077e9d1193b1d6d22b2485bf008208f10376774`

```dockerfile
```

-	Layers:
	-	`sha256:97ba1da3e9ec828f3aaf3930e06277f76cd0ccc27fabadf3381c724b461aaf89`  
		Last Modified: Tue, 13 Jan 2026 07:13:12 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a2a55a05b62dc316ccc44feb478292e528f3362b0debb2aaf523d42653b3df`  
		Last Modified: Tue, 13 Jan 2026 07:13:13 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:84c8e10910f255e60c176ba0a0f30b400616ac93ca3edfa9f8227e7c0ed96fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162662662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543953a3f2321265df54b334c16aa6c2fe706cfc80cc60ce48ca4155ba9414f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:16:12 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 13 Jan 2026 04:16:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:16:12 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:16:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:16:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:16:12 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdbccbaf6a168145824d1651dbd7bc7faac38ee214625f5254dd4ba9ead0bda`  
		Last Modified: Tue, 13 Jan 2026 04:16:30 GMT  
		Size: 18.9 MB (18885794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843e0b344a4e5351f09818b295ac69324493def6f22025377d20e3c48ece0ead`  
		Last Modified: Tue, 13 Jan 2026 04:16:29 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc471d4d4e54147d425df5f41fce09a21689fa62c1d37e05acdb637857f8b6`  
		Last Modified: Tue, 13 Jan 2026 04:16:44 GMT  
		Size: 71.8 MB (71800302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceac2ee0ef56101139e946f40b0b2b638560545fa3e79b6cae94f3eb48a2c7e`  
		Last Modified: Tue, 13 Jan 2026 04:16:38 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:bff5e5ce8f6cf610d484bf76ece253fabb3ddb3d72328323656b05bb7fe571c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cec4f699b0d21d66ff3e493aa657f4f50350dd414df54567b07a1605294bc2e`

```dockerfile
```

-	Layers:
	-	`sha256:41a15faea4f2bf19478b93a8c2c8afdfd69450b630d282c4b3e7c0f127911b78`  
		Last Modified: Tue, 13 Jan 2026 07:13:50 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f73686bfc571b066a9e6a7d4bd7e36247d13672bfc9539e3765389d88c59f7`  
		Last Modified: Tue, 13 Jan 2026 07:13:51 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Fri, 16 Jan 2026 19:05:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:26 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Fri, 16 Jan 2026 22:00:56 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:23 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Tue, 20 Jan 2026 12:36:13 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Tue, 20 Jan 2026 12:36:13 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Fri, 16 Jan 2026 22:00:50 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Fri, 16 Jan 2026 22:00:51 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Fri, 16 Jan 2026 22:00:53 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Fri, 16 Jan 2026 22:00:50 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:02:40 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:02:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:83d195c4add1fd9c007ea615b6d9b40a0ac697db59fb29de6de5a6473880c7bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37` - linux; amd64

```console
$ docker pull telegraf@sha256:1b67107eb22f74c20aa02013bee4f87f2519bf1372cb3b855c926d42b86c195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171887257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed79d27bdf37ff327ea262b678210d79f8d1b10bcbe35b42ed1e3d22859f7090`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:15:38 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:15:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:15:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:15:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:15:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:15:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:15 GMT  
		Size: 18.9 MB (18944358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab2a7d8ff7a8b31e5c31b4609fc0dabc473b9ac8d3ee6fc4e7192ed837333a3`  
		Last Modified: Tue, 13 Jan 2026 04:16:15 GMT  
		Size: 80.4 MB (80418714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791edbb052b74780373ba485bf7a4feb3bb37d9ad652d602d7d6e5de5920ffa6`  
		Last Modified: Tue, 13 Jan 2026 04:16:04 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:206454ec5d4fc5bb3ecb1a7564c1f5068c3ca9e05e04f11bcaecafa553eb2363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7830de8b8a27ee75cda6b3183aa293d5d2fcd2b2ab0f47bc0ed05eb3a9a904a1`

```dockerfile
```

-	Layers:
	-	`sha256:868ea599b3dc86abf95441916a311fd1ed9fff9c5ddb6d9051e4b681a66dde3c`  
		Last Modified: Tue, 13 Jan 2026 07:13:19 GMT  
		Size: 6.7 MB (6667266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dd78928881e651720705b5acc9a4b061a061f30f8ef57937b491e886bf928e`  
		Last Modified: Tue, 13 Jan 2026 07:13:20 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cf62ac35ce9687face50fd2639feb43a822a1aadc56849ea6c60b22501a6b414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158129223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e3b71af3c7c76e337b1db47ed652ce2d1be21c262c65e89ecf32cac729f3e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:43:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d9de7ad08dcb55771b6ddde8b11f6be1cab673bc19b2c17a508afcf0e038fe`  
		Last Modified: Tue, 13 Jan 2026 04:43:48 GMT  
		Size: 17.7 MB (17699967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd328b63edbfc32eae2bdc1cc9e3b04b04526a41ff244097abe4ae2ccf35e2`  
		Last Modified: Tue, 13 Jan 2026 04:43:44 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2b991059e5fc2e044e861b3c4b17e51e5060c3b3866144670a8ba2808738eb`  
		Last Modified: Tue, 13 Jan 2026 04:43:38 GMT  
		Size: 74.3 MB (74283228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70bfa42881d9120c2c8521d7af4537f02fbf0603426a3e0b88be6c6a773248f`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:12ddfd8a917b929e25e6d5a67b84236c387e7395f1e2224cc9df15ee37e517c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29413c178f6b4e8dbe33aef6c179252b1cc41587b29c8bf31fe73c50dab95f25`

```dockerfile
```

-	Layers:
	-	`sha256:d2d9dff5bd5b655aec0dd0a533e719c6d1a8fc2f0ba622b7c710730c0acf45c1`  
		Last Modified: Tue, 13 Jan 2026 07:13:26 GMT  
		Size: 6.7 MB (6661871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa7f8059928d92ad74587569e803f4e0bd49de8de136b0abf82bd8ea2d59a25`  
		Last Modified: Tue, 13 Jan 2026 07:13:31 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f4c3d34c2117855b765fc6ab55ddcbd18060947c3e4152ea0d153e5f01b8d744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162699196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222238f10efc3711dd1b91f23cd70340d8a502f075045cf7e847d9f0ad1e189`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:16:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:16:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:16:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f7cbd96129b6fe638c7445bd8e2d1feb2351c39c441cb6e4656c875eaaa763`  
		Last Modified: Tue, 13 Jan 2026 04:17:11 GMT  
		Size: 18.9 MB (18885863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9665c1a1012bd21135067154f34f8085d8bcafe3f80ba1a3d4091d3928f2c6a1`  
		Last Modified: Tue, 13 Jan 2026 04:17:09 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c513cd1aae42d831f532155229109d5de42c70bcd3bf42dc76847bcc6d056d`  
		Last Modified: Tue, 13 Jan 2026 04:17:14 GMT  
		Size: 71.8 MB (71836751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bc6b85aa14ae3bdea476987de5dc960351fe30f485a8290cfe46e6c86fb7a`  
		Last Modified: Tue, 13 Jan 2026 04:17:09 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:0cae81db187414977bbf6df94a1c9f06d4b37b32ed1722bc81ebf6acb5f0a231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca0e5160738313c1dbe3a4798f13851db641b8d4ab9b51299aa4d3297f89a62`

```dockerfile
```

-	Layers:
	-	`sha256:986540288d4f9cf6d63c77d17d075503218d155f061f23003d753f0c762daeae`  
		Last Modified: Tue, 13 Jan 2026 07:13:37 GMT  
		Size: 6.7 MB (6667954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555625d870c82a28b771e67bc00bb4b2e4408a81747cfda2e574b11d2d329cde`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:da425d612a6562dd10e0c451e6c4eb8afd167cdc57f3c6e8e9671eef96970b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b34930ce34197c6817195c87a9ceb42ac71e7aa324dfaa3020c38242a3c91947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86579178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c4937d4147e1e76854674e70f7a078d846f280232f989a537f1bf798e0d439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:03:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:03:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0006f07fa7aa837946a8af5d498120b48885b0a5a02c9929d7a1551c00c35f79`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34baf35d0c044c243bbbaefc8624d74fafaaf5352d5fcac982da66fd6eb5a22d`  
		Last Modified: Mon, 12 Jan 2026 22:04:21 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09297e8e447d6e5d15537473611c206598fe67e40163f9df8f6a70625ed054a`  
		Last Modified: Mon, 12 Jan 2026 22:04:43 GMT  
		Size: 80.2 MB (80212211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f557f91ca62469816ba86af69d33a347b7a268757860c5c75ee5a2b37c91aa`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7192889210b0d2a19dcf67c8c58ec2760bb49329e21c2e59cba027ec86a4fd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b96b7453f34b1b9c00194ce3f030a6c778a2e35b0d98a50c2ab271cd872f17`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f695b0d400877243266abe78ae2bd0a13b3f9fe68b331458a2e88db9b2be`  
		Last Modified: Mon, 12 Jan 2026 22:10:37 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0988d676a18b75ab875f5be5d1fdf99d16a05b1ba44dd7b33021b01eca13e07b`  
		Last Modified: Mon, 12 Jan 2026 22:10:38 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0763e04a854f82c70f01060f43ef8410836173a3b8d1c24de2ad347c882cc89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78396849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5cfe6009708d43fead662b5b2158f07259261ec4bb2f04b8578dd0d55ea70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:04:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:04:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1301b68b009329cd05b051fd8942099cfca0f90d771fa70b9d1dc51b4a8c4a`  
		Last Modified: Mon, 12 Jan 2026 22:04:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669d920cdb42e86e3e59b78a7f8edc2a98f16b82d01d5e8ad2efc4da60b6bb36`  
		Last Modified: Mon, 12 Jan 2026 22:04:39 GMT  
		Size: 2.6 MB (2627638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462024f532776566fd3272f6a12fef0a525de3afa955d8a7052c5d10e0dce9ca`  
		Last Modified: Mon, 12 Jan 2026 22:04:41 GMT  
		Size: 71.6 MB (71630243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679e78c84ba62ae726d2097b1e5bbed0c24b995736a357f7606235e33fb2fc6`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:846491217fca7d5ec7c094397cfbcdbabc951b578490d0d5518d83f37e2eb565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60147038d2ac3bedd7de0f47888bc221f044e9564bf3a8b19440b62a384a54`

```dockerfile
```

-	Layers:
	-	`sha256:62bc1c5598388899ccad1663492c6cca79651b20470c658d4f5cc43650d0a291`  
		Last Modified: Mon, 12 Jan 2026 22:04:39 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3919d3cbeb355252044e48eb284dbdd17931390f6452ecf5e3079f9e19006c1`  
		Last Modified: Mon, 12 Jan 2026 22:04:38 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.1`

```console
$ docker pull telegraf@sha256:83d195c4add1fd9c007ea615b6d9b40a0ac697db59fb29de6de5a6473880c7bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.1` - linux; amd64

```console
$ docker pull telegraf@sha256:1b67107eb22f74c20aa02013bee4f87f2519bf1372cb3b855c926d42b86c195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171887257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed79d27bdf37ff327ea262b678210d79f8d1b10bcbe35b42ed1e3d22859f7090`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:15:38 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:15:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:15:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:15:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:15:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:15:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:15 GMT  
		Size: 18.9 MB (18944358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab2a7d8ff7a8b31e5c31b4609fc0dabc473b9ac8d3ee6fc4e7192ed837333a3`  
		Last Modified: Tue, 13 Jan 2026 04:16:15 GMT  
		Size: 80.4 MB (80418714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791edbb052b74780373ba485bf7a4feb3bb37d9ad652d602d7d6e5de5920ffa6`  
		Last Modified: Tue, 13 Jan 2026 04:16:04 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:206454ec5d4fc5bb3ecb1a7564c1f5068c3ca9e05e04f11bcaecafa553eb2363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7830de8b8a27ee75cda6b3183aa293d5d2fcd2b2ab0f47bc0ed05eb3a9a904a1`

```dockerfile
```

-	Layers:
	-	`sha256:868ea599b3dc86abf95441916a311fd1ed9fff9c5ddb6d9051e4b681a66dde3c`  
		Last Modified: Tue, 13 Jan 2026 07:13:19 GMT  
		Size: 6.7 MB (6667266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dd78928881e651720705b5acc9a4b061a061f30f8ef57937b491e886bf928e`  
		Last Modified: Tue, 13 Jan 2026 07:13:20 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cf62ac35ce9687face50fd2639feb43a822a1aadc56849ea6c60b22501a6b414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158129223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e3b71af3c7c76e337b1db47ed652ce2d1be21c262c65e89ecf32cac729f3e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:43:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d9de7ad08dcb55771b6ddde8b11f6be1cab673bc19b2c17a508afcf0e038fe`  
		Last Modified: Tue, 13 Jan 2026 04:43:48 GMT  
		Size: 17.7 MB (17699967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd328b63edbfc32eae2bdc1cc9e3b04b04526a41ff244097abe4ae2ccf35e2`  
		Last Modified: Tue, 13 Jan 2026 04:43:44 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2b991059e5fc2e044e861b3c4b17e51e5060c3b3866144670a8ba2808738eb`  
		Last Modified: Tue, 13 Jan 2026 04:43:38 GMT  
		Size: 74.3 MB (74283228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70bfa42881d9120c2c8521d7af4537f02fbf0603426a3e0b88be6c6a773248f`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:12ddfd8a917b929e25e6d5a67b84236c387e7395f1e2224cc9df15ee37e517c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29413c178f6b4e8dbe33aef6c179252b1cc41587b29c8bf31fe73c50dab95f25`

```dockerfile
```

-	Layers:
	-	`sha256:d2d9dff5bd5b655aec0dd0a533e719c6d1a8fc2f0ba622b7c710730c0acf45c1`  
		Last Modified: Tue, 13 Jan 2026 07:13:26 GMT  
		Size: 6.7 MB (6661871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa7f8059928d92ad74587569e803f4e0bd49de8de136b0abf82bd8ea2d59a25`  
		Last Modified: Tue, 13 Jan 2026 07:13:31 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f4c3d34c2117855b765fc6ab55ddcbd18060947c3e4152ea0d153e5f01b8d744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162699196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222238f10efc3711dd1b91f23cd70340d8a502f075045cf7e847d9f0ad1e189`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:16:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:16:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:16:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f7cbd96129b6fe638c7445bd8e2d1feb2351c39c441cb6e4656c875eaaa763`  
		Last Modified: Tue, 13 Jan 2026 04:17:11 GMT  
		Size: 18.9 MB (18885863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9665c1a1012bd21135067154f34f8085d8bcafe3f80ba1a3d4091d3928f2c6a1`  
		Last Modified: Tue, 13 Jan 2026 04:17:09 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c513cd1aae42d831f532155229109d5de42c70bcd3bf42dc76847bcc6d056d`  
		Last Modified: Tue, 13 Jan 2026 04:17:14 GMT  
		Size: 71.8 MB (71836751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bc6b85aa14ae3bdea476987de5dc960351fe30f485a8290cfe46e6c86fb7a`  
		Last Modified: Tue, 13 Jan 2026 04:17:09 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:0cae81db187414977bbf6df94a1c9f06d4b37b32ed1722bc81ebf6acb5f0a231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca0e5160738313c1dbe3a4798f13851db641b8d4ab9b51299aa4d3297f89a62`

```dockerfile
```

-	Layers:
	-	`sha256:986540288d4f9cf6d63c77d17d075503218d155f061f23003d753f0c762daeae`  
		Last Modified: Tue, 13 Jan 2026 07:13:37 GMT  
		Size: 6.7 MB (6667954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555625d870c82a28b771e67bc00bb4b2e4408a81747cfda2e574b11d2d329cde`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.1-alpine`

```console
$ docker pull telegraf@sha256:da425d612a6562dd10e0c451e6c4eb8afd167cdc57f3c6e8e9671eef96970b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b34930ce34197c6817195c87a9ceb42ac71e7aa324dfaa3020c38242a3c91947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86579178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c4937d4147e1e76854674e70f7a078d846f280232f989a537f1bf798e0d439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:03:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:03:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0006f07fa7aa837946a8af5d498120b48885b0a5a02c9929d7a1551c00c35f79`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34baf35d0c044c243bbbaefc8624d74fafaaf5352d5fcac982da66fd6eb5a22d`  
		Last Modified: Mon, 12 Jan 2026 22:04:21 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09297e8e447d6e5d15537473611c206598fe67e40163f9df8f6a70625ed054a`  
		Last Modified: Mon, 12 Jan 2026 22:04:43 GMT  
		Size: 80.2 MB (80212211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f557f91ca62469816ba86af69d33a347b7a268757860c5c75ee5a2b37c91aa`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7192889210b0d2a19dcf67c8c58ec2760bb49329e21c2e59cba027ec86a4fd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b96b7453f34b1b9c00194ce3f030a6c778a2e35b0d98a50c2ab271cd872f17`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f695b0d400877243266abe78ae2bd0a13b3f9fe68b331458a2e88db9b2be`  
		Last Modified: Mon, 12 Jan 2026 22:10:37 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0988d676a18b75ab875f5be5d1fdf99d16a05b1ba44dd7b33021b01eca13e07b`  
		Last Modified: Mon, 12 Jan 2026 22:10:38 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0763e04a854f82c70f01060f43ef8410836173a3b8d1c24de2ad347c882cc89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78396849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5cfe6009708d43fead662b5b2158f07259261ec4bb2f04b8578dd0d55ea70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:04:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:04:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1301b68b009329cd05b051fd8942099cfca0f90d771fa70b9d1dc51b4a8c4a`  
		Last Modified: Mon, 12 Jan 2026 22:04:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669d920cdb42e86e3e59b78a7f8edc2a98f16b82d01d5e8ad2efc4da60b6bb36`  
		Last Modified: Mon, 12 Jan 2026 22:04:39 GMT  
		Size: 2.6 MB (2627638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462024f532776566fd3272f6a12fef0a525de3afa955d8a7052c5d10e0dce9ca`  
		Last Modified: Mon, 12 Jan 2026 22:04:41 GMT  
		Size: 71.6 MB (71630243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679e78c84ba62ae726d2097b1e5bbed0c24b995736a357f7606235e33fb2fc6`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:846491217fca7d5ec7c094397cfbcdbabc951b578490d0d5518d83f37e2eb565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60147038d2ac3bedd7de0f47888bc221f044e9564bf3a8b19440b62a384a54`

```dockerfile
```

-	Layers:
	-	`sha256:62bc1c5598388899ccad1663492c6cca79651b20470c658d4f5cc43650d0a291`  
		Last Modified: Mon, 12 Jan 2026 22:04:39 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3919d3cbeb355252044e48eb284dbdd17931390f6452ecf5e3079f9e19006c1`  
		Last Modified: Mon, 12 Jan 2026 22:04:38 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:da425d612a6562dd10e0c451e6c4eb8afd167cdc57f3c6e8e9671eef96970b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b34930ce34197c6817195c87a9ceb42ac71e7aa324dfaa3020c38242a3c91947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86579178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c4937d4147e1e76854674e70f7a078d846f280232f989a537f1bf798e0d439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:03:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:03:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0006f07fa7aa837946a8af5d498120b48885b0a5a02c9929d7a1551c00c35f79`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34baf35d0c044c243bbbaefc8624d74fafaaf5352d5fcac982da66fd6eb5a22d`  
		Last Modified: Mon, 12 Jan 2026 22:04:21 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09297e8e447d6e5d15537473611c206598fe67e40163f9df8f6a70625ed054a`  
		Last Modified: Mon, 12 Jan 2026 22:04:43 GMT  
		Size: 80.2 MB (80212211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f557f91ca62469816ba86af69d33a347b7a268757860c5c75ee5a2b37c91aa`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7192889210b0d2a19dcf67c8c58ec2760bb49329e21c2e59cba027ec86a4fd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b96b7453f34b1b9c00194ce3f030a6c778a2e35b0d98a50c2ab271cd872f17`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f695b0d400877243266abe78ae2bd0a13b3f9fe68b331458a2e88db9b2be`  
		Last Modified: Mon, 12 Jan 2026 22:10:37 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0988d676a18b75ab875f5be5d1fdf99d16a05b1ba44dd7b33021b01eca13e07b`  
		Last Modified: Mon, 12 Jan 2026 22:10:38 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0763e04a854f82c70f01060f43ef8410836173a3b8d1c24de2ad347c882cc89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78396849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5cfe6009708d43fead662b5b2158f07259261ec4bb2f04b8578dd0d55ea70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:04:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:04:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1301b68b009329cd05b051fd8942099cfca0f90d771fa70b9d1dc51b4a8c4a`  
		Last Modified: Mon, 12 Jan 2026 22:04:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669d920cdb42e86e3e59b78a7f8edc2a98f16b82d01d5e8ad2efc4da60b6bb36`  
		Last Modified: Mon, 12 Jan 2026 22:04:39 GMT  
		Size: 2.6 MB (2627638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462024f532776566fd3272f6a12fef0a525de3afa955d8a7052c5d10e0dce9ca`  
		Last Modified: Mon, 12 Jan 2026 22:04:41 GMT  
		Size: 71.6 MB (71630243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679e78c84ba62ae726d2097b1e5bbed0c24b995736a357f7606235e33fb2fc6`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:846491217fca7d5ec7c094397cfbcdbabc951b578490d0d5518d83f37e2eb565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60147038d2ac3bedd7de0f47888bc221f044e9564bf3a8b19440b62a384a54`

```dockerfile
```

-	Layers:
	-	`sha256:62bc1c5598388899ccad1663492c6cca79651b20470c658d4f5cc43650d0a291`  
		Last Modified: Mon, 12 Jan 2026 22:04:39 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3919d3cbeb355252044e48eb284dbdd17931390f6452ecf5e3079f9e19006c1`  
		Last Modified: Mon, 12 Jan 2026 22:04:38 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:83d195c4add1fd9c007ea615b6d9b40a0ac697db59fb29de6de5a6473880c7bc
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
$ docker pull telegraf@sha256:1b67107eb22f74c20aa02013bee4f87f2519bf1372cb3b855c926d42b86c195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171887257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed79d27bdf37ff327ea262b678210d79f8d1b10bcbe35b42ed1e3d22859f7090`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:15:38 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:15:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:15:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:15:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:15:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:15:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:15 GMT  
		Size: 18.9 MB (18944358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab2a7d8ff7a8b31e5c31b4609fc0dabc473b9ac8d3ee6fc4e7192ed837333a3`  
		Last Modified: Tue, 13 Jan 2026 04:16:15 GMT  
		Size: 80.4 MB (80418714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791edbb052b74780373ba485bf7a4feb3bb37d9ad652d602d7d6e5de5920ffa6`  
		Last Modified: Tue, 13 Jan 2026 04:16:04 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:206454ec5d4fc5bb3ecb1a7564c1f5068c3ca9e05e04f11bcaecafa553eb2363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7830de8b8a27ee75cda6b3183aa293d5d2fcd2b2ab0f47bc0ed05eb3a9a904a1`

```dockerfile
```

-	Layers:
	-	`sha256:868ea599b3dc86abf95441916a311fd1ed9fff9c5ddb6d9051e4b681a66dde3c`  
		Last Modified: Tue, 13 Jan 2026 07:13:19 GMT  
		Size: 6.7 MB (6667266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dd78928881e651720705b5acc9a4b061a061f30f8ef57937b491e886bf928e`  
		Last Modified: Tue, 13 Jan 2026 07:13:20 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cf62ac35ce9687face50fd2639feb43a822a1aadc56849ea6c60b22501a6b414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158129223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e3b71af3c7c76e337b1db47ed652ce2d1be21c262c65e89ecf32cac729f3e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:43:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d9de7ad08dcb55771b6ddde8b11f6be1cab673bc19b2c17a508afcf0e038fe`  
		Last Modified: Tue, 13 Jan 2026 04:43:48 GMT  
		Size: 17.7 MB (17699967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd328b63edbfc32eae2bdc1cc9e3b04b04526a41ff244097abe4ae2ccf35e2`  
		Last Modified: Tue, 13 Jan 2026 04:43:44 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2b991059e5fc2e044e861b3c4b17e51e5060c3b3866144670a8ba2808738eb`  
		Last Modified: Tue, 13 Jan 2026 04:43:38 GMT  
		Size: 74.3 MB (74283228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70bfa42881d9120c2c8521d7af4537f02fbf0603426a3e0b88be6c6a773248f`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:12ddfd8a917b929e25e6d5a67b84236c387e7395f1e2224cc9df15ee37e517c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29413c178f6b4e8dbe33aef6c179252b1cc41587b29c8bf31fe73c50dab95f25`

```dockerfile
```

-	Layers:
	-	`sha256:d2d9dff5bd5b655aec0dd0a533e719c6d1a8fc2f0ba622b7c710730c0acf45c1`  
		Last Modified: Tue, 13 Jan 2026 07:13:26 GMT  
		Size: 6.7 MB (6661871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa7f8059928d92ad74587569e803f4e0bd49de8de136b0abf82bd8ea2d59a25`  
		Last Modified: Tue, 13 Jan 2026 07:13:31 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f4c3d34c2117855b765fc6ab55ddcbd18060947c3e4152ea0d153e5f01b8d744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162699196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222238f10efc3711dd1b91f23cd70340d8a502f075045cf7e847d9f0ad1e189`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:16:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:16:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:16:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f7cbd96129b6fe638c7445bd8e2d1feb2351c39c441cb6e4656c875eaaa763`  
		Last Modified: Tue, 13 Jan 2026 04:17:11 GMT  
		Size: 18.9 MB (18885863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9665c1a1012bd21135067154f34f8085d8bcafe3f80ba1a3d4091d3928f2c6a1`  
		Last Modified: Tue, 13 Jan 2026 04:17:09 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c513cd1aae42d831f532155229109d5de42c70bcd3bf42dc76847bcc6d056d`  
		Last Modified: Tue, 13 Jan 2026 04:17:14 GMT  
		Size: 71.8 MB (71836751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bc6b85aa14ae3bdea476987de5dc960351fe30f485a8290cfe46e6c86fb7a`  
		Last Modified: Tue, 13 Jan 2026 04:17:09 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0cae81db187414977bbf6df94a1c9f06d4b37b32ed1722bc81ebf6acb5f0a231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca0e5160738313c1dbe3a4798f13851db641b8d4ab9b51299aa4d3297f89a62`

```dockerfile
```

-	Layers:
	-	`sha256:986540288d4f9cf6d63c77d17d075503218d155f061f23003d753f0c762daeae`  
		Last Modified: Tue, 13 Jan 2026 07:13:37 GMT  
		Size: 6.7 MB (6667954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555625d870c82a28b771e67bc00bb4b2e4408a81747cfda2e574b11d2d329cde`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
