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
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d901276e8d660c9c3643003d1099eedd64836cf2c857706c853224234cd680`  
		Last Modified: Tue, 13 Jan 2026 04:16:27 GMT  
		Size: 18.9 MB (18885851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2359d97ce7c58015c1632ff80cc75cd613494d5d320ef65198fecd11fac54c`  
		Last Modified: Tue, 13 Jan 2026 04:17:03 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:55 GMT  
		Size: 6.6 MB (6648479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4ad23d8a413616ad24fc4267913b6977d019eeea06d3f3c7cec66fc6892cbf`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:1c67d350b4b97e6ef2c52d04c5a2b606038700b27c30be1fcc827c83d0750a90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9d4345e1cbea1692800b2bca89494a285dcdaa455d92ab5477366cf36c9c2e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85738081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3597a88f010efa8c7ae4f264f02c6ad85d626f9a0eefc21ccaf48540739cff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:40 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
ENV TELEGRAF_VERSION=1.35.4
# Wed, 28 Jan 2026 03:49:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db80302b016defca3353492ca7c69f65db624dc6d54d024637ba8ba208850ef`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e58ddbb2a68e9d1ec1a1d042347ef3b4855d97c57682045f6270d4d6ce65e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 2.6 MB (2563630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee38868a04a63efb19c32997823ce073d4d9be80d4e550105f70e2ae1bf16aca`  
		Last Modified: Wed, 28 Jan 2026 03:50:06 GMT  
		Size: 79.4 MB (79368676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea97445439cc0d1b2cc6a71d85464903745b6178429c75c2d2d7e0171384e2`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:445328e3ce2e66cb85d892cc6b99f7798d01a4486949a22c5d6d2f2069a7db7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb527adc4e3ce61db447b66ae5adbdb2f7ec85f40b0c52e579cc26e2647fc0d`

```dockerfile
```

-	Layers:
	-	`sha256:d9182e5ff44eee6bc219f9e41785816ff8d2e9fc6e8bebcb6467e56cba51cfb7`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b292c7a96e63a10e77e2dd531cb8e17f1217bf8984cfbfdff44ce7a0d80632`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9bb580f67318869d8c3bbffd0a74ae79e9f956146bc92e373cf53f84e9e8b083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78645343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee82eedad832ef0ab6940d14b7abb701ba0cf8236e54281c11563a70abcf95b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:55:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:55:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
ENV TELEGRAF_VERSION=1.35.4
# Wed, 28 Jan 2026 03:56:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765c2e9488726202408b292c3bac6681d93508efc6e9b2e31e049443567e86e0`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3740b37ea70449e245a9450fc906cc28ba6b7da57b398514750aacfc86b1d6`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 2.6 MB (2627594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1aca9cb457419a7597e00416afd07021750d63f302bb9c4682cfed96fe6e60`  
		Last Modified: Wed, 28 Jan 2026 03:56:17 GMT  
		Size: 71.9 MB (71877331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73362025389d6291b89519a9ae98aaf7933a67f20ce60d58dc6f6fb3c319fd8`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5a1d3b60fe8ea0f375b2edd76de7b0562a301c54a6c16b659996e1309d5e66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75036200048cf02c5b626a83dd60adfc0691bb3e378a6f72fb6611670b0d4fbf`

```dockerfile
```

-	Layers:
	-	`sha256:e9293a685398b5fdd11336f57a7027774d95fcd5ed44adff467f472929367767`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c0437ff9d4a470eaa9b4e3b11c362bdff43f1305a03cc25a83c8655dcbcf9d`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 15.0 KB (15028 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d901276e8d660c9c3643003d1099eedd64836cf2c857706c853224234cd680`  
		Last Modified: Tue, 13 Jan 2026 04:16:27 GMT  
		Size: 18.9 MB (18885851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2359d97ce7c58015c1632ff80cc75cd613494d5d320ef65198fecd11fac54c`  
		Last Modified: Tue, 13 Jan 2026 04:17:03 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:55 GMT  
		Size: 6.6 MB (6648479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4ad23d8a413616ad24fc4267913b6977d019eeea06d3f3c7cec66fc6892cbf`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:1c67d350b4b97e6ef2c52d04c5a2b606038700b27c30be1fcc827c83d0750a90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9d4345e1cbea1692800b2bca89494a285dcdaa455d92ab5477366cf36c9c2e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85738081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3597a88f010efa8c7ae4f264f02c6ad85d626f9a0eefc21ccaf48540739cff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:40 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
ENV TELEGRAF_VERSION=1.35.4
# Wed, 28 Jan 2026 03:49:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db80302b016defca3353492ca7c69f65db624dc6d54d024637ba8ba208850ef`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e58ddbb2a68e9d1ec1a1d042347ef3b4855d97c57682045f6270d4d6ce65e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 2.6 MB (2563630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee38868a04a63efb19c32997823ce073d4d9be80d4e550105f70e2ae1bf16aca`  
		Last Modified: Wed, 28 Jan 2026 03:50:06 GMT  
		Size: 79.4 MB (79368676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea97445439cc0d1b2cc6a71d85464903745b6178429c75c2d2d7e0171384e2`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:445328e3ce2e66cb85d892cc6b99f7798d01a4486949a22c5d6d2f2069a7db7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb527adc4e3ce61db447b66ae5adbdb2f7ec85f40b0c52e579cc26e2647fc0d`

```dockerfile
```

-	Layers:
	-	`sha256:d9182e5ff44eee6bc219f9e41785816ff8d2e9fc6e8bebcb6467e56cba51cfb7`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b292c7a96e63a10e77e2dd531cb8e17f1217bf8984cfbfdff44ce7a0d80632`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9bb580f67318869d8c3bbffd0a74ae79e9f956146bc92e373cf53f84e9e8b083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78645343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee82eedad832ef0ab6940d14b7abb701ba0cf8236e54281c11563a70abcf95b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:55:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:55:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
ENV TELEGRAF_VERSION=1.35.4
# Wed, 28 Jan 2026 03:56:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765c2e9488726202408b292c3bac6681d93508efc6e9b2e31e049443567e86e0`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3740b37ea70449e245a9450fc906cc28ba6b7da57b398514750aacfc86b1d6`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 2.6 MB (2627594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1aca9cb457419a7597e00416afd07021750d63f302bb9c4682cfed96fe6e60`  
		Last Modified: Wed, 28 Jan 2026 03:56:17 GMT  
		Size: 71.9 MB (71877331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73362025389d6291b89519a9ae98aaf7933a67f20ce60d58dc6f6fb3c319fd8`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5a1d3b60fe8ea0f375b2edd76de7b0562a301c54a6c16b659996e1309d5e66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75036200048cf02c5b626a83dd60adfc0691bb3e378a6f72fb6611670b0d4fbf`

```dockerfile
```

-	Layers:
	-	`sha256:e9293a685398b5fdd11336f57a7027774d95fcd5ed44adff467f472929367767`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c0437ff9d4a470eaa9b4e3b11c362bdff43f1305a03cc25a83c8655dcbcf9d`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 15.0 KB (15028 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:22 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a69654e2ff4e8a54881fef6c442c931ca21dbe768fd2c0514e4792a6db81ea`  
		Last Modified: Tue, 13 Jan 2026 04:15:25 GMT  
		Size: 80.5 MB (80473538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ba7f86dfedd6cc722fc54431ddaeb41939b733a71ee996b3a24d893480995c`  
		Last Modified: Tue, 13 Jan 2026 04:15:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3260264734f11a0dcf2c688e6b709c967bfbe661975d9620e42eedf009712d`  
		Last Modified: Tue, 13 Jan 2026 04:43:30 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:43:28 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a2a55a05b62dc316ccc44feb478292e528f3362b0debb2aaf523d42653b3df`  
		Last Modified: Tue, 13 Jan 2026 04:43:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:16:32 GMT  
		Size: 71.8 MB (71800302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceac2ee0ef56101139e946f40b0b2b638560545fa3e79b6cae94f3eb48a2c7e`  
		Last Modified: Tue, 13 Jan 2026 04:16:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:16:30 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f73686bfc571b066a9e6a7d4bd7e36247d13672bfc9539e3765389d88c59f7`  
		Last Modified: Tue, 13 Jan 2026 04:16:29 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:22 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a69654e2ff4e8a54881fef6c442c931ca21dbe768fd2c0514e4792a6db81ea`  
		Last Modified: Tue, 13 Jan 2026 04:15:25 GMT  
		Size: 80.5 MB (80473538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ba7f86dfedd6cc722fc54431ddaeb41939b733a71ee996b3a24d893480995c`  
		Last Modified: Tue, 13 Jan 2026 04:15:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3260264734f11a0dcf2c688e6b709c967bfbe661975d9620e42eedf009712d`  
		Last Modified: Tue, 13 Jan 2026 04:43:30 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:43:28 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a2a55a05b62dc316ccc44feb478292e528f3362b0debb2aaf523d42653b3df`  
		Last Modified: Tue, 13 Jan 2026 04:43:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:16:32 GMT  
		Size: 71.8 MB (71800302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceac2ee0ef56101139e946f40b0b2b638560545fa3e79b6cae94f3eb48a2c7e`  
		Last Modified: Tue, 13 Jan 2026 04:16:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:16:30 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f73686bfc571b066a9e6a7d4bd7e36247d13672bfc9539e3765389d88c59f7`  
		Last Modified: Tue, 13 Jan 2026 04:16:29 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:06 GMT  
		Size: 18.9 MB (18944358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab2a7d8ff7a8b31e5c31b4609fc0dabc473b9ac8d3ee6fc4e7192ed837333a3`  
		Last Modified: Tue, 13 Jan 2026 04:15:59 GMT  
		Size: 80.4 MB (80418714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791edbb052b74780373ba485bf7a4feb3bb37d9ad652d602d7d6e5de5920ffa6`  
		Last Modified: Tue, 13 Jan 2026 04:15:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:57 GMT  
		Size: 6.7 MB (6667266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dd78928881e651720705b5acc9a4b061a061f30f8ef57937b491e886bf928e`  
		Last Modified: Tue, 13 Jan 2026 04:15:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:43:37 GMT  
		Size: 17.7 MB (17699967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd328b63edbfc32eae2bdc1cc9e3b04b04526a41ff244097abe4ae2ccf35e2`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 6.7 MB (6661871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa7f8059928d92ad74587569e803f4e0bd49de8de136b0abf82bd8ea2d59a25`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f7cbd96129b6fe638c7445bd8e2d1feb2351c39c441cb6e4656c875eaaa763`  
		Last Modified: Tue, 13 Jan 2026 04:17:01 GMT  
		Size: 18.9 MB (18885863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9665c1a1012bd21135067154f34f8085d8bcafe3f80ba1a3d4091d3928f2c6a1`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c513cd1aae42d831f532155229109d5de42c70bcd3bf42dc76847bcc6d056d`  
		Last Modified: Tue, 13 Jan 2026 04:17:04 GMT  
		Size: 71.8 MB (71836751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bc6b85aa14ae3bdea476987de5dc960351fe30f485a8290cfe46e6c86fb7a`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:17:01 GMT  
		Size: 6.7 MB (6667954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555625d870c82a28b771e67bc00bb4b2e4408a81747cfda2e574b11d2d329cde`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:98d238fac269c949f0574ed7a1fec403b1acf79be4f0c4ec38941f94de1d566a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f532da2eb8b819a3a270f9c751e89331da81c86940bfd27281f8b85eb85eaff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86581620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b2b5dd6c4243f44d050b74b97814e4de1cb50fd8b9ebd1b8f1b291e5c179de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:49:45 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710e8ea768bc4c5628c8e56d287d7a67720c9b15bde9850b70d0a05723f51936`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ad1e390f36b724abd91aa22a28eb46c025163a62dc0911807357e78154a8e`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 80.2 MB (80212230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9551f385152eb62f889eeac14aa6f4c2a25647891cda4c7c90f2ca653dd93ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1e3ddddbda26a225a059e6e2a379518112e670d949e6f7abecba16226be11b`

```dockerfile
```

-	Layers:
	-	`sha256:881320f646701d701accef70533b21fd01b1228efa3f5a08799dac74e5fb5bc4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f4f5b027d0939ab896d19fef833e0975aa6b329dc393c086859740b7cdc765`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ddc91fe454b27a2b140a694c51938b3634275cf386cb9bb5a06a3c814fe4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78398298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e03eca0c8ec323879f457dc6137397bd850cccee5c292654e3601eae5febacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:12 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15ea420ed678b641ffe5a2375797d77f159e1c6d7d7bc21dd50e5ba6c40e4e4`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979f17c250ed04c44e760bb1df516f6382cc558c1de3b324a98ab37d99229ee`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 2.6 MB (2627628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d72b6efebcdd0e2dd86e573eabc9bb26ef060fd1601036f495294ede9ae77`  
		Last Modified: Wed, 28 Jan 2026 03:56:33 GMT  
		Size: 71.6 MB (71630252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684706cc32aedd8438e6eeab7b7b636b198f3f53cc99cf7357028c3b3a7ca505`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8e4fdf60c586a5bd4b42c2a03ebc59c0f42921f887cf6b64620d69d21a3ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720d80d3926d8e1a966a4f920c28b6479880e8acdabe11d3c83c7a4382220f9`

```dockerfile
```

-	Layers:
	-	`sha256:3ed6e0a713bc070c69819eda05cc98e39c8ff92c5aa86971557bed38cbc3901a`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726dbaed541995327adbca51afdd5d39292bfeeb2b73c30ee45a231287dcd04d`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 15.3 KB (15341 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:06 GMT  
		Size: 18.9 MB (18944358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab2a7d8ff7a8b31e5c31b4609fc0dabc473b9ac8d3ee6fc4e7192ed837333a3`  
		Last Modified: Tue, 13 Jan 2026 04:15:59 GMT  
		Size: 80.4 MB (80418714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791edbb052b74780373ba485bf7a4feb3bb37d9ad652d602d7d6e5de5920ffa6`  
		Last Modified: Tue, 13 Jan 2026 04:15:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:57 GMT  
		Size: 6.7 MB (6667266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dd78928881e651720705b5acc9a4b061a061f30f8ef57937b491e886bf928e`  
		Last Modified: Tue, 13 Jan 2026 04:15:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:43:37 GMT  
		Size: 17.7 MB (17699967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd328b63edbfc32eae2bdc1cc9e3b04b04526a41ff244097abe4ae2ccf35e2`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 6.7 MB (6661871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa7f8059928d92ad74587569e803f4e0bd49de8de136b0abf82bd8ea2d59a25`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f7cbd96129b6fe638c7445bd8e2d1feb2351c39c441cb6e4656c875eaaa763`  
		Last Modified: Tue, 13 Jan 2026 04:17:01 GMT  
		Size: 18.9 MB (18885863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9665c1a1012bd21135067154f34f8085d8bcafe3f80ba1a3d4091d3928f2c6a1`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c513cd1aae42d831f532155229109d5de42c70bcd3bf42dc76847bcc6d056d`  
		Last Modified: Tue, 13 Jan 2026 04:17:04 GMT  
		Size: 71.8 MB (71836751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bc6b85aa14ae3bdea476987de5dc960351fe30f485a8290cfe46e6c86fb7a`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:17:01 GMT  
		Size: 6.7 MB (6667954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555625d870c82a28b771e67bc00bb4b2e4408a81747cfda2e574b11d2d329cde`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.1-alpine`

```console
$ docker pull telegraf@sha256:98d238fac269c949f0574ed7a1fec403b1acf79be4f0c4ec38941f94de1d566a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f532da2eb8b819a3a270f9c751e89331da81c86940bfd27281f8b85eb85eaff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86581620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b2b5dd6c4243f44d050b74b97814e4de1cb50fd8b9ebd1b8f1b291e5c179de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:49:45 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710e8ea768bc4c5628c8e56d287d7a67720c9b15bde9850b70d0a05723f51936`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ad1e390f36b724abd91aa22a28eb46c025163a62dc0911807357e78154a8e`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 80.2 MB (80212230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9551f385152eb62f889eeac14aa6f4c2a25647891cda4c7c90f2ca653dd93ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1e3ddddbda26a225a059e6e2a379518112e670d949e6f7abecba16226be11b`

```dockerfile
```

-	Layers:
	-	`sha256:881320f646701d701accef70533b21fd01b1228efa3f5a08799dac74e5fb5bc4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f4f5b027d0939ab896d19fef833e0975aa6b329dc393c086859740b7cdc765`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ddc91fe454b27a2b140a694c51938b3634275cf386cb9bb5a06a3c814fe4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78398298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e03eca0c8ec323879f457dc6137397bd850cccee5c292654e3601eae5febacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:12 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15ea420ed678b641ffe5a2375797d77f159e1c6d7d7bc21dd50e5ba6c40e4e4`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979f17c250ed04c44e760bb1df516f6382cc558c1de3b324a98ab37d99229ee`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 2.6 MB (2627628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d72b6efebcdd0e2dd86e573eabc9bb26ef060fd1601036f495294ede9ae77`  
		Last Modified: Wed, 28 Jan 2026 03:56:33 GMT  
		Size: 71.6 MB (71630252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684706cc32aedd8438e6eeab7b7b636b198f3f53cc99cf7357028c3b3a7ca505`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8e4fdf60c586a5bd4b42c2a03ebc59c0f42921f887cf6b64620d69d21a3ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720d80d3926d8e1a966a4f920c28b6479880e8acdabe11d3c83c7a4382220f9`

```dockerfile
```

-	Layers:
	-	`sha256:3ed6e0a713bc070c69819eda05cc98e39c8ff92c5aa86971557bed38cbc3901a`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726dbaed541995327adbca51afdd5d39292bfeeb2b73c30ee45a231287dcd04d`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 15.3 KB (15341 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:98d238fac269c949f0574ed7a1fec403b1acf79be4f0c4ec38941f94de1d566a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f532da2eb8b819a3a270f9c751e89331da81c86940bfd27281f8b85eb85eaff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86581620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b2b5dd6c4243f44d050b74b97814e4de1cb50fd8b9ebd1b8f1b291e5c179de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:49:45 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710e8ea768bc4c5628c8e56d287d7a67720c9b15bde9850b70d0a05723f51936`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ad1e390f36b724abd91aa22a28eb46c025163a62dc0911807357e78154a8e`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 80.2 MB (80212230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9551f385152eb62f889eeac14aa6f4c2a25647891cda4c7c90f2ca653dd93ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1e3ddddbda26a225a059e6e2a379518112e670d949e6f7abecba16226be11b`

```dockerfile
```

-	Layers:
	-	`sha256:881320f646701d701accef70533b21fd01b1228efa3f5a08799dac74e5fb5bc4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f4f5b027d0939ab896d19fef833e0975aa6b329dc393c086859740b7cdc765`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ddc91fe454b27a2b140a694c51938b3634275cf386cb9bb5a06a3c814fe4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78398298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e03eca0c8ec323879f457dc6137397bd850cccee5c292654e3601eae5febacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:12 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15ea420ed678b641ffe5a2375797d77f159e1c6d7d7bc21dd50e5ba6c40e4e4`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979f17c250ed04c44e760bb1df516f6382cc558c1de3b324a98ab37d99229ee`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 2.6 MB (2627628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d72b6efebcdd0e2dd86e573eabc9bb26ef060fd1601036f495294ede9ae77`  
		Last Modified: Wed, 28 Jan 2026 03:56:33 GMT  
		Size: 71.6 MB (71630252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684706cc32aedd8438e6eeab7b7b636b198f3f53cc99cf7357028c3b3a7ca505`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8e4fdf60c586a5bd4b42c2a03ebc59c0f42921f887cf6b64620d69d21a3ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720d80d3926d8e1a966a4f920c28b6479880e8acdabe11d3c83c7a4382220f9`

```dockerfile
```

-	Layers:
	-	`sha256:3ed6e0a713bc070c69819eda05cc98e39c8ff92c5aa86971557bed38cbc3901a`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726dbaed541995327adbca51afdd5d39292bfeeb2b73c30ee45a231287dcd04d`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 15.3 KB (15341 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935094610ce99926e3ad19dc959593e1e5d50b4973cc8a43e9d8cd0e303b59e`  
		Last Modified: Tue, 13 Jan 2026 04:15:06 GMT  
		Size: 18.9 MB (18944358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac0dc3896d69f3de90ac4499eeb7650e673667c195808a08e1002f0c10979`  
		Last Modified: Tue, 13 Jan 2026 04:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab2a7d8ff7a8b31e5c31b4609fc0dabc473b9ac8d3ee6fc4e7192ed837333a3`  
		Last Modified: Tue, 13 Jan 2026 04:15:59 GMT  
		Size: 80.4 MB (80418714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791edbb052b74780373ba485bf7a4feb3bb37d9ad652d602d7d6e5de5920ffa6`  
		Last Modified: Tue, 13 Jan 2026 04:15:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:57 GMT  
		Size: 6.7 MB (6667266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dd78928881e651720705b5acc9a4b061a061f30f8ef57937b491e886bf928e`  
		Last Modified: Tue, 13 Jan 2026 04:15:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:43:37 GMT  
		Size: 17.7 MB (17699967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd328b63edbfc32eae2bdc1cc9e3b04b04526a41ff244097abe4ae2ccf35e2`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 6.7 MB (6661871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa7f8059928d92ad74587569e803f4e0bd49de8de136b0abf82bd8ea2d59a25`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f7cbd96129b6fe638c7445bd8e2d1feb2351c39c441cb6e4656c875eaaa763`  
		Last Modified: Tue, 13 Jan 2026 04:17:01 GMT  
		Size: 18.9 MB (18885863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9665c1a1012bd21135067154f34f8085d8bcafe3f80ba1a3d4091d3928f2c6a1`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c513cd1aae42d831f532155229109d5de42c70bcd3bf42dc76847bcc6d056d`  
		Last Modified: Tue, 13 Jan 2026 04:17:04 GMT  
		Size: 71.8 MB (71836751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bc6b85aa14ae3bdea476987de5dc960351fe30f485a8290cfe46e6c86fb7a`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:17:01 GMT  
		Size: 6.7 MB (6667954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555625d870c82a28b771e67bc00bb4b2e4408a81747cfda2e574b11d2d329cde`  
		Last Modified: Tue, 13 Jan 2026 04:17:00 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
